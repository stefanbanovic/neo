<template>
  <section class="contact-image">
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>Contact us</h1>
          <h3>Get in touch with us</h3>
        </div>
      </div>
    </div>
  </section>
  <section class="contact">
    <div class="container">
      <div class="row">
        <div class="col">
          <form>
            <input type="text" autocomplete="off" placeholder="Name" name="name">
            <input type="text" autocomplete="off" placeholder="Subject" name="subject">
            <textarea placeholder="Your message" name="msg"></textarea>
            <button type="submit" @click.prevent="showMsg">Send</button>
          </form>
          <p>{{ msg }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Contact',
  data() {
    return {
      msg: ''
    }
  },
  methods: {
    showMsg() {
      this.msg = 'We will pretend that email is sent.';
    }
  }
}
</script>
<style lang="scss" scoped>
section.contact-image {
  display:flex;
  align-items: center;
  justify-content: center;
  height: 40vh;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.5), rgba(127, 121, 111, 0.5)), url("https://images.pexels.com/photos/1122156/pexels-photo-1122156.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260");
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
section.contact {
    padding: 100px 0;
    background: #efefef;

  .col {
    width: 50%;
    align-self: center;
  }

  h1 {
    font-size: 30px;
    font-weight: bold;
    text-transform: uppercase;
  }

  form {
    display: flex;
    flex-direction: column;
    margin-top: 50px;
    color: #efefef;

    input {
      margin: 20px 0;
      height: 80px;
      background: #d6d6d6;
      color: #333;
      font-size: 20px;
      padding: 0 15px;
      border: none;
      outline: none;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    textarea {
      margin: 20px 0;
      background: #d6d6d6;
      color: #333;
      font-size: 20px;
      padding: 15px;
      border: 0;
      outline: 0;
      max-width: 100%;
      min-width: 100%;
      min-height: 300px;
      font-family: inherit;
      resize: none;
    }

    button {
      margin: 20px 0;
      background: #333;
      color: #efefef;
      height: 80px;
      font-size: 20px;
      padding: 15px;
      border: none;
      outline: none;
    }
  }

  @media (max-width: 768px) {
    
    .col {
      width: 90%;
    }
  }
}
</style>