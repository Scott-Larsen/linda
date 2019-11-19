<template>
  <div>
    <Nav/>
    <nuxt />
  </div>
</template>

<script>
import Nav from './partials/nav';
export default {
  components: {
    Nav
  }
}
</script>

<style lang="scss">

$color-pink: #f7e4ed;
$color-grey: #303030;
$color-grey: black;
$color-olive-green: #445525;

$color-Copper-Dark: #2B0D04;
$color-Copper-Mid-Dark: #553623;
$color-Copper-Mid-Light: #7E5E42;
$color-Copper-Light: #A88761;

@function shade($color, $percentage) {
  @return mix(Black, $color, $percentage);
}

body  {
  background-image: url("~assets/Ferris-Wheel-Orig-Clear.gif");
  background-repeat: no-repeat;
  background-position: right bottom;
  background-size: 24rem;



  color: $color-grey;
  background-color: $color-pink; /* For browsers that do not support gradients */
  padding: 0;
  margin: 0;
  font-size: 62.5%;
  font-family: serif, Palatino, Georgia, Times;
  font-display: auto;
  line-height: 2.5em;
  margin: auto;
  padding: 10px;
  
  a {
    color: $color-olive-green;
  
  &:hover, &:active, &:visited {
        color: shade($color-olive-green, 25%);
  }
 } 
}

.container {
  background: rgba(255, 255, 255, 0.8);
  padding: .5em;
  border-radius: 1.4rem;
  font-size: 1.7em;
}

.header {
  background-image: linear-gradient(170deg, $color-Copper-Light 12%, $color-Copper-Mid-Light 38%, $color-Copper-Dark 65%, $color-Copper-Mid-Light 80%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    color: #fff;
  position: relative;
  text-align: center;
  
	font-size: 15.25vw;
  line-height: 18vw;
}

.header, nav {
  font-family: 'Cinzel-auto', serif;
  font-display: auto;
}

h2 {
  color: $color-olive-green;
  margin-top: .5em;
  line-height: 1.25em;
}

.book-title-line {
  font-size: 1em;
  margin: 1em 0 1.5em 0;
  line-height: 1.25em;
}

.book-title {
  font-size: 1.25em;
  color: $color-olive-green;
}

.date {
  font-style: italic;
  font-size: .8em;
  line-height: 2em;
}

.sidebar-image  {
  margin: 0 0 .75em 2em;
  float: right;
}

img {
  border: 1px solid black;
}

.entry-footer {
  font-size: .85em;
}

input, textarea {
    font-size: 1em;
    padding: .55em .8em;
    border-radius: 5px;
}

button {
  font-size: 1.3em;
  background-color: #f7dae8;
  border-color: $color-pink;
  padding: 0.3em 2em;
  border-radius: .75em;

  &:hover {
  background-color: $color-pink;
  }

}


nav {
  font-size: 2em;
  position: -webkit-sticky;
  position: sticky;
  top: 0; 
  z-index: 2;
        
  ul {
    min-width: 13em;
    text-align: justify;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 0; padding: 0;
    background-color: $color-pink;
    filter: alpha(opacity=20); /* For IE8 and earlier */
    
    li {
      position: relative;
      display: inline-block;
    }
    
    a {
      color: $color-grey;
      padding: 5px;
      display: block;

      &:hover {
        background-color: #f7dae8;
        border-radius: .3em;
        text-decoration: underline;
      }
    }

    .subnav {
      background-color: $color-pink;
      visibility: hidden;
      flex-direction: column;
      position: absolute;
      left: 0; 
      top: 99%;
      border-radius: .3em;
    }

    .has-subnav:hover .subnav,
    .has-subnav:focus .subnav,
    .has-subnav:focus-within .subnav,
    .subnav:hover {
      visibility: visible;
    }
  }
}

.wrapper {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}

  @media only screen and (min-device-width: 720px) and (orientation: landscape) {
       
  body {
    background-size: 35rem;
    width: 700px !important;
  }
  
  .header {
    
	font-size: 7.9vw;
  line-height: 6.6vw;
  padding-top: 30px;
  }
  
  .container {
  background: rgba(255, 255, 255, 0.8);
  padding: 2em;
  }
    
  nav {
    ul {
    flex-wrap: nowrap;
      li  {
        a   {
          padding: 15px;
      text-decoration: none;
        }
      }
    }
  }

  }



  @media screen and (max-width: 522px) /* Mobile */ {


    background-size: 18rem;

  nav ul li ul li:first-child {
    padding-top: 2em;
  }
  }


</style>
