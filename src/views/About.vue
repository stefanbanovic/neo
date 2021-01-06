<template>
  <section class="about-company">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>About our Company</h1>
          <h3>Let us introduce you to our work</h3>
        </div>
      </div>
    </div>
  </section>
  <section class="introduction-part">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Introduction</h1>
          <h3>Just another subtitle</h3>
          <div>
            <p><b>Lorem ipsum </b><br>dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<br><br>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
            <div><img src="https://images.pexels.com/photos/2058147/pexels-photo-2058147.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="needs-part">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Suit your needs</h1>
          <h3>This part of page is a subtitle</h3>
          <div class="needs">
            <div class="need">
              <img src="https://images.pexels.com/photos/2058147/pexels-photo-2058147.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
              <p>Data managing</p>
            </div>
            <div class="need">
              <img src="https://images.pexels.com/photos/159888/pexels-photo-159888.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
              <p>Analytics</p>
            </div>
            <div class="need">
              <img src="https://images.pexels.com/photos/2058138/pexels-photo-2058138.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
              <p>Taxes</p>
            </div>
            <div class="need">
              <img src="https://images.pexels.com/photos/3285196/pexels-photo-3285196.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
              <p>Professional Consluting</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="news-part">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Lastest news</h1>
          <h3>Just another subtitle</h3>
          <div>
            <p><b>Lorem ipsum </b><br>dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<br><br>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.<span><router-link to="/news">Check our latest news<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="white" d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"/></svg></router-link></span></p>
            <div><img src="https://images.pexels.com/photos/159888/pexels-photo-159888.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section.about-company {
  display:flex;
  align-items: center;
  justify-content: center;
  height: 40vh;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.5), rgba(127, 121, 111, 0.5)), url("https://images.pexels.com/photos/3285196/pexels-photo-3285196.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260");
  background-size: cover;
  background-position: center;
  color: white;
    
    .col {
      align-items: center;
    }

    img {
      width: 150px;
    }

    h1 {
      font-size: 50px;
      margin-bottom: 20px;
      color: inherit;
    }
    h3 {
      color: inherit;
    }
}

section.introduction-part {
    padding: 50px 0 0 0;
    background: #efefef;

    .col {
      width: 80%;
      align-self: center;

      h1 {
        font-size: 30px;
        font-weight: bold;
        text-transform: uppercase;
      }

      div {
        display: flex;
        margin: 100px 0 0 0;
        height: 500px;

        p{
          display: flex;
          flex: 0 1 50%;
          flex-direction: column;
          text-align: justify;
          background: #333;
          color: white;
          padding: 50px;
          margin: 0;


          b {
            font-size: 25px;
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

      .col div {
        
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

section.needs-part {
    padding: 50px 0 0 0;

    .col {
      width: 75%;
      align-self: center;
    }
    
    h1 {
      font-size: 30px;
      font-weight: bold;
      text-transform: uppercase;
    }

    .needs {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 50px;
      flex:1;
    

      .need {
        display: flex;
        flex:1;
        flex-direction: column;
        height: 400px;
        overflow: hidden;
        position: relative;
        background: rgba(0, 0, 0, 0.5);

        &:hover {

          p {
            transform: translateY(-20px);
          }

          img {
            transform: translateY(-10px);
          }
        }
        img {
          height: 150%;
          width: auto;
          position: absolute;
          z-index: -1;
          transition: .3s all;
          transition-delay: .1s;
        }

        p {
          position: absolute;
          bottom: 0;
          color: white;
          font-size: 20px;
          font-weight: bold;
          padding: 5px 10px;
          transition: .3s all;
        }
      }
    }

    @media(max-width: 768px){

    .needs {
      flex-direction: column;

      .need {
        flex: auto;
        width: 100%;
      }
    }
  }
}

section.news-part {
    padding: 50px 0;
    background: #efefef;

    .col {
      width: 80%;
      align-self: center;

      h1 {
        font-size: 30px;
        font-weight: bold;
        text-transform: uppercase;
      }

      div {
        display: flex;
        margin: 100px 0;
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

      .col div {
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
</style>