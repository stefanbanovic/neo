<template>
  <header>
        <a id="logo">
            <router-link to="/">
                <img src="../assets/logo-white.svg">
            </router-link>
        </a>
        <button class="navbar-toggle" data-target="#mobilemenu" data-toggle="collapse" type="button" :class="{ 'toggle-active': isActive }" @click="isActive = !isActive">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
        </button>
        <nav :class="{ 'toggle-active': isActive }">
        <ul id="nav">
            <li id="home">
                <router-link to="/">Home</router-link>
            </li>
            <li id="about">
                <router-link to="/about">About</router-link>
            </li>
            <li id="news">
                <router-link to="/news">News</router-link>
            </li>
            <li id="contact">
                <router-link to="/contact">Contact</router-link>
            </li>
        </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      isActive: false
    }
  },
  methods: {
      toggleClass() {
          this.isActive != this.isActive;
      }
  }

}
</script>

<style lang="scss" scoped>
header {
    background: #0071bc;
    display: flex;
    flex:1;
    position: fixed;
    width: 100%;
    top: 0;
    padding: 0 15px;
    z-index: 1;

    a#logo {
        display: flex;
        flex: 1;
        align-items: center;;

        img{
            width: 45px;
            height: 45px;
        }
    }
    nav {
        display: flex;
        flex: 1;
        align-items: center;
    }

    ul {
        display: flex;
        flex:2;
        align-items: center;


        li{
            display: flex;
            list-style: none;
        }

    }

    ul#nav {
        flex: auto;
        justify-content: space-evenly;
        padding: 30px;
    
      a {
        font-weight: bold;
        color: white;
        text-decoration: none;

            &:hover, &.router-link-exact-active {
                color: #152b3a;
            }
        }
    }


/* Menu animation */

.navbar-toggle {
    width: 34px;
    height: 29px;
    margin: 0;
    display: none;
    position: relative;
    margin-right: 15px;
    padding: 0;
    margin-top: 8px;
    outline: 0;
    border: 0;
    margin-bottom: 8px;
    background-color: transparent;
    border: 1px solid transparent;

        span.icon-bar {
        width: 100%;
        height: 4px;
        background: white;
        display: block;
        position: relative;
        -webkit-transition: all .3s;
        transition: all .3s;

        &:first-child {
            position: absolute;
            top: 0;
            -webkit-transform: translateY(0px);
            transform: translateY(0px);
            -webkit-transition: all .3s;
            transition: all .3s;
            -webkit-transition-delay: .6s;
            transition-delay: .6s;
        }

        &:nth-child(2) {
            position: absolute;
            top: 50%;
            margin-top: -2px;
            -webkit-transition: all .3s;
            transition: all .3s;
            -webkit-transition-delay: .6s;
            transition-delay: .6s;
        }

        &:last-child {
            position: absolute;
            bottom: 0;
            -webkit-transform: translateY(0px);
            transform: translateY(0px);
            -webkit-transition: all .3s;
            transition: all .3s;
            -webkit-transition-delay: .6s;
            transition-delay: .6s;
        }

        &:nth-child(2){

            &::before {
                content: '';
                width: 100%;
                height: 4px;
                background: white;
                display: block;
                position: absolute;
                -webkit-transform: rotateZ(0deg);
                transform: rotateZ(0deg);
                -webkit-transition: all .3s cubic-bezier(0.65, 0.05, 0.36, 1);
                transition: all .3s cubic-bezier(0.65, 0.05, 0.36, 1);
                -webkit-transition-delay: .3s;
                transition-delay: .3s;
            }
            &::after {
                content: '';
                width: 100%;
                height: 4px;
                background: white;
                display: block;
                position: absolute;
                -webkit-transform: rotateZ(0deg);
                transform: rotateZ(0deg);
                -webkit-transition: all .3s cubic-bezier(0.65, 0.05, 0.36, 1);
                transition: all .3s cubic-bezier(0.65, 0.05, 0.36, 1);
                -webkit-transition-delay: .3s;
                transition-delay: .3s;
            }
        }
    }
}


.navbar-toggle.toggle-active span.icon-bar {

    &:first-child {
        height: 0px;
        -webkit-transform: translateY(6px);
        transform: translateY(6px);
        -webkit-transition: all .3s;
        transition: all .3s;
    }

    &:nth-child(2) {
        height: 0px;
        -webkit-transition: all .3s;
        transition: all .3s;
    }

    &:nth-child(2) {

        &::before {
            -webkit-transform: rotateZ(405deg);
            transform: rotateZ(405deg);
            -webkit-transition: all .3s;
            transition: all .3s;
            -webkit-transition-delay: .3s;
            transition-delay: .3s;
        }

        &::after {
            -webkit-transform: rotateZ(-405deg);
            transform: rotateZ(-405deg);
            -webkit-transition: all .3s;
            transition: all .3s;
            -webkit-transition-delay: .3s;
            transition-delay: .3s;
        }
    }

    &:last-child {
        height: 0px;
        -webkit-transform: translateY(-6px);
        transform: translateY(-6px);
        -webkit-transition: all .3s;
        transition: all .3s;
    }
}

@media(max-width: 768px){
    
    flex-wrap: wrap;
    padding: 0;

    a#logo img {
        display: flex;
        align-items: center;
        height: 80px;
        margin-left: 15px;
    }
    nav {
        flex: 1 1 100%;
        border-top: 1px solid white;
        height: 0;
        transition: all 0.25s ease-out;
        
        
        ul#nav {
            flex-direction: column;

             li {
                font-size: 0px;
            }
        }

        &.toggle-active {
            transition: all 0.25s ease-in;
            height: 200px;
            
            ul#nav li {
                font-size: inherit;
                transition-delay: .2s;
                margin: 10px 0;
            }
        }
    }

    .navbar-toggle {
        display: flex;
        align-self: center;
    }
}

}
</style>