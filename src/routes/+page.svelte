<script>
	import Heading from "../components/Heading.svelte"
    let {click_number} = $state(0)

    function score_add() {
        click_number += 1
    }

    function emoji(){
        if (button.innerText = "🙂") {
            click_number += 1
            button.innerText = "😢"
        } else {
            click_number -= 1
            button.innerText = "🙂"
        }
    }

</script>

<div class="headings">
    <!-- <Heading {message}= "Svelte"/> 
    <Heading {message}= "je"/>
    <Heading {message}= "brnkačka"/>  --> 
</div>

<div class="container">
    <p>Score: {click_number}</p> 
    <div class="buttons">
        <button onclick={score_add}>+</button>
        <button onclick={emoji}>🙂</button>
    </div>
</div>

<!-- {#if (click_number > 5){
    Heading.style.visibility = visible
}} -->



<style>
* {
    font-family: monospace;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    gap: 10px;
}

.container > p {
    font-size: 2em;
}

.buttons > button{
    border: 1px solid black;
    border-radius: 50000px;
    padding: 10px 20px;
    background-color: lightblue;
    font-size: 1.5em;
}

.buttons > button:nth-of-type(1) {
    background-color: lightblue;
}

.buttons > button:nth-of-type(2) {
    background-color: lightcoral;
}

.headings {
    position: absolute;
}

:global(.headings > h2) {
	position: absolute;
    font-size: 3em;

}

:global(.headings > h2:nth-child(1)) {
	left: 300px;
	top: 50px;
}

:global(.headings > h2:nth-child(2)) {
	left: 200px;
	top: 200px;
}

:global(.headings > h2:nth-child(3)) {
	left: 300px;
	top: 350px;
}


</style>