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

<button on:click={() => ilike('cats')}>
  I like cats 
</button>
<button on:click={() => ilike('horses')}>
  I like horses 
</button>
<button on:click={() => ilike('dogs')}>
  I like dogs 
</button>
<p>
{likes}
</p>
