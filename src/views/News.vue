<template>
  <section class="news">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Lastest news</h1>
          <h3>Just another subtitle</h3>
          <div>
            <p><b>News number 1 </b><br>dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<br><br>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<span><router-link to="/news" @click.prevent="showMsg1">Read more<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="white" d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/></svg></router-link></span>{{ msg1 }}</p>
            <div><img src="https://images.pexels.com/photos/159888/pexels-photo-159888.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></div>
          </div>
        </div>
        <div class="col">
          <div>
            <p><b>News number 2 </b><br>dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<br><br>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<span><router-link to="/news" @click.prevent="showMsg2">Read more<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="white" d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/></svg></router-link></span>{{ msg2 }}</p>
            <div><img src="https://images.pexels.com/photos/159888/pexels-photo-159888.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></div>
          </div>
        </div>
        <div class="col">
          <div>
            <p><b>News number 3 </b><br>dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<br><br>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<span><router-link to="/news" @click.prevent="showMsg3">Read more<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="white" d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/></svg></router-link></span>{{ msg3 }}</p>
            <div><img src="https://images.pexels.com/photos/159888/pexels-photo-159888.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'News',
  data() {
    return {
      msg1: '',
      msg2: '',
      msg3: ''
    }
  },
  methods: {
    showMsg1() {
      this.msg1 = 'This would lead you to article page 1'
    },
    showMsg2() {
      this.msg2 = 'This would lead you to article page 2'
    },
    showMsg3() {
      this.msg3 = 'This would lead you to article page 3'
    }
  }
}
</script>
<style lang="scss" scoped>
section.news {
    padding: 50px 0;
    background: #efefef;

    .col {
      width: 80%;
      align-self: center;

    &:nth-child(odd) div {
      flex-direction: row-reverse;
    }

      h1 {
        font-size: 30px;
        font-weight: bold;
        text-transform: uppercase;
      }

      div {
        display: flex;
        margin: 50px 0;
        height: 500px;

        p{
          display: flex;
          flex: 0 1 50%;
          flex-direction: column;
          text-align: justify;
          background: #808080;
          color: white;
          padding: 50px;
          margin: 0;


          b {
            font-size: 25px;
          }

          a {
            display: flex;
            align-items: center;
            margin-top: 50px;
            font-size: 20px;
            color: white;
            text-decoration: none;

            &:hover svg{

              transform: translateX(10px);
            }
            svg {
              transition: .3s all;
              margin-left: 20px;
            }
          }
        }

        div {
          display: flex;
          flex: 1 1 50%;
          margin: 0;
          overflow: hidden;

          img {
            height: 200%;
         }
        }
      }
    }

  @media(max-width: 768px){

    .col {

      &:nth-child(odd) div {
        flex-direction: column-reverse;
      }
      
      div {
        flex-direction: column;
        height: auto;

        p {
          flex: 1 0 100%;
        }

        div {
          flex: 1 0 100%;
          height: 400px;

          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>