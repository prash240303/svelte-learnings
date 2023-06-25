<script>
  const hugss = "<h1> huggs to </h1>";
  const disabled = true;
  const status = "success";
  let isPromoted = false;
  let num = 1;
  function changeStyle() {
    if (num % 2 == 0) {
      isPromoted = true;
    } else {
      isPromoted = false;
    }
    num++;
    console.log(num);
  }
  let name = '' ;
  let nums = 0 ;
  let displayNames = []; // Array to store the names to be displayed

  function handleClick()
  {
	if(!name == '' )
	{
		nums++;
		displayNames = [...displayNames, name]
	}
  }


</script>

<main>
  <div class="div">
    <!-- <button {disabled}>this is a disabled button</button> -->
  
  <!-- <h1 class="underline">this is underlined text</h1>
  <h2 class={status}>this is danger text</h2>
  <button on:click={changeStyle}>change the style </button>
  <h2 class={isPromoted ? "promoted" : ""}>movie title</h2>
  <input type="text" name="name" id="name" bind:value={name}/> -->

	<h1 class="heading">Enter your name here</h1>
  <form on:submit|preventDefault>
    <input type="text" bind:value={name} class="input" placeholder="Enter your name" />
    <button on:click={handleClick} class="button-74" >Submit</button>
  </form>

  <p class="note">you can click as many times and recive the message</p> 
  {#if displayNames.length > 0}
    {#each displayNames as displayName}
      <p class="message">biggg huggss 🫂🫂🫂  to {displayName}</p>
    {/each}
  {/if}


</div>


</main>


<style>
	@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,500&display=swap');
  /* .underline {
    text-decoration: underline;
  }
  .danger {
    color: #ff3e00;
  }
  .success {
    color: olivedrab;
  }
  .promoted {
    font-style: italic;
  } */
.div{
	background: #FFDEF2;
	font-family: 'Playfair Display', serif;
    text-align: center;
    padding-top: 3rem;
	border: 2px solid black;
    margin:20px ;
	border-radius: 30px;  box-shadow: #422800 4px 4px 0 0;
	height: 85vh;
	
}
.note {
	font-size: 18px;
	font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.heading{
	font-family: 'Playfair Display', serif;	display: block;
	font-weight: 400;
}

  .input{
	background-color: #fbeee0;
  border: 2px solid #422800;
  border-radius: 30px;
  box-shadow: #422800 4px 4px 0 0;
  color: #422800;
  cursor: pointer;
  display: inline-block;
  font-weight: 600;
  margin-right: 20px;
  font-size: 18px;
  padding: 0 18px;
  line-height: 50px;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  }
 
  .input:hover {
  background-color: #fff;
}
/* CSS */
.button-74 {
  background-color: #fbeee0;
  border: 2px solid #422800;
  border-radius: 30px;
  box-shadow: #422800 4px 4px 0 0;
  color: #422800;
  cursor: pointer;
  display: inline-block;
  font-weight: 600;
  font-size: 18px;
  padding: 0 18px;
  line-height: 50px;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-74:hover {
  background-color: #fff;
}

.button-74:active {
  box-shadow: #422800 2px 2px 0 0;
  transform: translate(2px, 2px);
}
.input::selection {
  box-shadow: #422800 2px 2px 0 0;
  transform: translate(2px, 2px);
  border: none;
  border-style: none;
}
.message{
	display: block;
  font-weight: 600;
  font-size: 32px;
  padding: 0 18px;
  line-height: 50px;
  text-align: center;
  text-decoration: none;
}

@media (min-width: 768px) {
  .button-74 {
    min-width: 120px;
    padding: 0 25px;
  }}
  /* h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  } */
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
