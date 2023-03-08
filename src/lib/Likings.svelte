<script>
  let likes = []
  const ilike = (topic) => {
    if(!likes.includes(topic)){
      likes = [...likes, topic]
      
        fetch(`https://fake-ad-server.herokuapp.com/cookie/${topic}`,{
            credentials: 'include' 
         })
          .then(response => {
    // process data
    console.log('got it ', response)
  })
  .catch(error => {
    console.error('Panic at the disco:', error);
  })
     

    }
  }
</script>

<button on:click={() => ilike('specific_car1')}>
  I like specific_car1 
</button>
<button on:click={() => ilike('read_houses')}>
  I like read_houses 
</button>
<button on:click={() => ilike('Motorola phones')}>
  I like Motorola phones 
</button>
<p>
{likes}
</p>
