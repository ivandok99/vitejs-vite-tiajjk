<script>
export default {
  data() {
    return {
      msg: 'Hello World!',
    };
  },
  methods: {
    async invio() {
      const response = await fetch('/api/auth/signin', {
        method: 'POST',
        body: new FormData(login),
      });
      console.log(FormData(login));
      console.log(response);
    },
  },
};
</script>

<template>
  <body>
    <div class="container">
      <h1>Welcome</h1>
      <form class="form" id="login">
        <input type="text" placeholder="Username" />
        <input type="password" placeholder="Password" />
        <button type="submit" @click="invio">Login</button>
      </form>
    </div>
  </body>
</template>

<style>
@font-face {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 200;
  src: url(https://fonts.gstatic.com/s/sourcesanspro/v21/6xKydSBYKcSV-LCoeQqfX1RYOo3i94_wlxdr.ttf)
    format('truetype');
}
@font-face {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 200;
  src: url(https://fonts.gstatic.com/s/sourcesanspro/v21/6xKydSBYKcSV-LCoeQqfX1RYOo3ik4zwlxdr.ttf)
    format('truetype');
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-weight: 300;
}
body {
  background-image: url('/bg.jpg');
  font-family: 'Source Sans Pro', sans-serif;
  /*color: white;*/
  font-weight: 300;
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  opacity: 1;
  color: white;
  /*background-size: cover;*/
}
/*body ::-webkit-input-placeholder {
    /* WebKit browsers 
    font-family: 'Source Sans Pro', sans-serif;
    color: white;
    font-weight: 300;

  }
  body :-moz-placeholder {
    /* Mozilla Firefox 4 to 18 
    font-family: 'Source Sans Pro', sans-serif;
    color: white;
    opacity: 1;
    font-weight: 300;

  }
  body ::-moz-placeholder {
    /* Mozilla Firefox 19+ 
    font-family: 'Source Sans Pro', sans-serif;
    color: white;
    opacity: 1;
    font-weight: 300;

  }
  body :-ms-input-placeholder {
    /* Internet Explorer 10+ 
    font-family: 'Source Sans Pro', sans-serif;
    color: white;
    font-weight: 300;

  }
  /*.wrapper.form-success .container h1 {
    transform: translateY(85px);
  }*/
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20% 0;
  height: 600px;
  text-align: center;
}
.container h1 {
  margin-bottom: 5%;
  font-size: 50px;
  transition-duration: 1s;
  transition-timing-function: ease-in-put;
  font-weight: 800;
}
form {
  padding: 20px 0;
  position: relative;
  z-index: 2;
}
form input {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  outline: 0;
  border: 1px solid rgba(255, 255, 255, 0.4);
  background-color: rgba(255, 255, 255, 0.2);
  width: 300px;
  border-radius: 3px;
  padding: 10px 15px;
  margin: 0 auto 10px auto;
  display: block;
  text-align: center;
  font-size: 18px;
  color: rgba(71, 71, 71, 1);
  transition-duration: 0.5s;
}
form ::placeholder {
  color: rgba(148, 148, 148, 1);
}
form input:hover {
  background-color: rgba(255, 255, 255, 0.4);
}
form input:focus {
  background-color: rgba(255, 255, 255, 0.7);
  width: 350px;
  color: black;
}
form button {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  outline: 0;
  background-color: white;
  border: 0;
  padding: 10px 15px;
  color: black /*rgba(144, 144, 231, 1)/*#53e3a6*/;
  border-radius: 3px;
  width: 300px;
  cursor: pointer;
  font-size: 19px;
  transition-duration: 0.25s;
}

/*@-webkit-keyframes square {
    0% {
      transform: translateY(0);
    }
    100% {
      transform: translateY(-700px) rotate(600deg);
    }
  }
  @keyframes square {
    0% {
      transform: translateY(0);
    }
    100% {
      transform: translateY(-700px) rotate(600deg);
    }
  }*/
</style>
