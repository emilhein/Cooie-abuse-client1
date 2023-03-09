<script>
  const ilike = (topic) => {
    fakeAdserver.insertAdIntoDiv(topic)
  }
</script>

<button on:click={() => ilike('carslot')}>

  I like Aston Martin
</button>
<button on:click={() => ilike('houseslot')}>
  I like red houses 
</button>
<button on:click={() => ilike('phonesslot')}>
  I like Motorola phones 
</button>
<p>
</p>
