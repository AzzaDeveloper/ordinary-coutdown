<script>
    import sf from 'seconds-formater';
    let timeLeft = "";
    function update() {
        timeLeft = sf.convert(1689422400 - (Date.now() / 1000)).format('D days HH hours M mins S secs')
    }

    update()
    setInterval(() => {
        update()
    }, 1000);
</script>
<svelte:head>
	<title>unORDINARY</title>
	<!-- Primary Meta Tags -->
	<meta name="title" content="unORDINARY" />
	<meta
		name="description"
		content="Countdown until the game releases."
	/>

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	
	<meta property="og:title" content="unORDINARY" />
	<meta
		property="og:description"
		content="Countdown until the game releases."
	/>
	<meta
		property="og:image"
		content="https://media.discordapp.net/attachments/1087690796611940352/1119928240824406016/unordinary-gfx.png"
	/>

	<!-- Twitter -->
	
	<meta property="twitter:title" content="unORDINARY" />
	<meta
		property="twitter:description"
		content="Countdown until the game releases."
	/>
	<meta
		property="twitter:image"
		content="https://media.discordapp.net/attachments/1087690796611940352/1119928240824406016/unordinary-gfx.png"
	/>
	<!-- Meta stuff-->
	
	<meta name="author" content="Cyfer" />
	<meta
		name="description"
		content="Countdown until the game releases."
	/>
</svelte:head>
<div id="logoContainer">
    <img id="logo" src="v1.png" alt="logo">
    <img id="alpha" src="alpha.png" alt="alpha">
</div>
<div id="timer">
    <div id="timerText">
        <b>{timeLeft}</b>
    </div>
</div>
<style>
    #logoContainer {
        text-align: center;
        margin-top: 0%;
    }
    #logo {
        width: 80%;
    }
    #alpha {
        margin-top: -15%;
        width: 40%;
    }
    #timer {
        padding: 25px;
        text-align: center;
        font-size: 75px;
        border: 2px solid white;
        border-radius: 25px;
        background: url(/polka.png) repeat , linear-gradient(#4c4a50, #141414);
        width: 75%;
        margin: auto;
        position: fixed;
        top: 80%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    #timerText {
        font-family: 'Lora', serif;
        background: linear-gradient(#ffffff, #504d4d);
        -webkit-text-stroke: #333036 0px;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }
</style>