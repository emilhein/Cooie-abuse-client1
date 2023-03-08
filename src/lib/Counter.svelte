<script>
  let likes = []
  const ilike = (topic) => {
    if(!likes.includes(topic)){
      likes = [...likes, topic]
      try {
        
        fetch(`https://expresssimpler53bqn-fdzy--80.local-credentialless.webcontainer.io/cookie/${topic}`)
          .then(response => {
    // process data
    console.log('got it ', response)
  })
  .catch(error => {
    console.error('Panic at the disco:', error);
  })
        }catch (error){
          console.log(error)
        }

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
