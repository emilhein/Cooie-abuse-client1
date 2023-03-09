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

<button on:click={() => ilike('aston_martin')}>
  I like Aston Martin
</button>
<button on:click={() => ilike('red_houses')}>
  I like red houses 
</button>
<button on:click={() => ilike('motorola_phones')}>
  I like Motorola phones 
</button>
<p>
{likes}
</p>
