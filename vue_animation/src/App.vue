<template>
    
	<body>

    <div class="wrapper">
        
        <input class="radio-button" type="radio" name="cube-image" checked>
        <input class="radio-button" type="radio" name="cube-image">
        <input class="radio-button" type="radio" name="cube-image">
        <input class="radio-button" type="radio" name="cube-image">
        <input class="radio-button" type="radio" name="cube-image">
        <input class="radio-button" type="radio" name="cube-image">
    
        <div class="cube">
            <div class="cube-side"></div>
            <div class="cube-side"></div>
            <div class="cube-side"></div>
            <div class="cube-side"></div>
            <div class="cube-side"></div>
            <div class="cube-side"></div>
        </div>
    </div>
   
</body>
</template>

<script>
	export default {
		name:'App',
	}
</script>

<style>

body {
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}


.wrapper {
    width: 15em;
    height: 15em;
    text-align: center;
    perspective: 45em;
}

.cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition-duration: 2s;
}

.cube-side {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: white;
    border: 1px solid black;
    background-position: center;
    background-size: cover;
    
}

.radio-button {
    margin-bottom: 6em;
}

.cube-side:nth-child(1) {
    transform: rotateY(0deg) translateZ(7.5em);
    background-image:url(1.jpg);

}
.cube-side:nth-child(2) {
    transform: rotateY(90deg) translateZ(7.5em);
    background-image: url(2.JPG);
}
.cube-side:nth-child(3) {
    transform: rotateY(180deg) translateZ(7.5em);
    background-image: url(3.JPG);
}
.cube-side:nth-child(4) {
    transform: rotateY(-90deg) translateZ(7.5em);
    background-image: url(4.JPG);
}
.cube-side:nth-child(5) {
    transform: rotateX(-90deg) translateZ(7.5em);
    background-image: url(5.jpg);
}
.cube-side:nth-child(6) {
    transform: rotateX(90deg) translateZ(7.5em);
    background-image: url(6.JPG);
}


.radio-button:checked ~ .cube {
    transition-duration: 3s;
    transition-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
}
.radio-button:nth-child(1):checked ~ .cube { 
    transform: rotateX(-15deg) rotateY(0deg);
}
.radio-button:nth-child(2):checked ~ .cube { 
    transform: rotateX(-15deg) rotateY(180deg);
}
.radio-button:nth-child(3):checked ~ .cube { 
    transform: rotateX(-15deg) rotateY(90deg);
}
.radio-button:nth-child(4):checked ~ .cube { 
    transform: rotateX(-15deg) rotateY(-90deg);
}
.radio-button:nth-child(5):checked ~ .cube { 
    transform: rotateX(-105deg) rotateY(0deg);
}
.radio-button:nth-child(6):checked ~ .cube { 
    transform: rotateX(75deg) rotateY(0deg);
}
</style>