<div class="container">
  <div class="content">
    <!-- <p class="hide-cursor">Jad Salameh</p>
        <p class="hide-cursor">Software Engeneer</p> -->
    <h1>Jad Salameh</h1>
    <h1>Software Engeneer</h1>
    <p class="hide-cursor">
      Lorem ipsum dolor sit amet consectetur adipisicing hhhhhhhhhhhhhhhhhhhhh
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit vel mollitia
      nisi beatae iure necessitatibus ea asperiores esse harum. Atque quaerat
      optio odit. Magni, similique voluptatem. Nam voluptate dolore autem.
    </p>
  </div>
</div>

<style>
  .container {
    /* background-color: green; */
    display: flex;
    justify-content: center;
    align-items: center;
    /* height: 100vh; */
  }
  .content {
    text-align: center;
  }

  @import url("https://fonts.googleapis.com/css?family=Source+Code+Pro");

  /* body {
        padding: 40px;
        background-color: #121212;
      } */

  p {
    /* border-right: solid 3px rgba(0, 255, 0, 0.75); */
    overflow: hidden;
    font-family: "Source Code Pro", monospace;
    font-size: 28px;
    color: black;
  }

  /* Animation */
  p {
    animation: animated-text 2s steps(29, end) 1s 1 normal both,
      animated-cursor 100ms steps(29, end) infinite;
  }

  /* text animation */
  @keyframes animated-text {
    from {
      width: 0;
    }
    to {
      width: 472px;
    }
  }

  /* cursor animations */
  @keyframes animated-cursor {
    from {
      border-right-color: rgba(0, 255, 0, 0.75);
    }
    to {
      border-right-color: transparent;
    }
  }

  @media (min-width: 500px) and (max-width: 643px) {
    h1 {
      font-size: 28px;
    }
    p {
      font-size: 20px;
    }
  }

  @media (min-width: 400px) and (max-width: 499px) {
    h1 {
      font-size: 26px;
    }
    p {
      font-size: 20px;
      /* width: 10%; */
    }

    @keyframes animated-text {
      from {
        width: 0;
      }
      to {
        width: 350px;
      }
    }
  }
  @media (min-width: 350px) and (max-width: 399px) {
    h1 {
      font-size: 26px;
    }
    p {
      font-size: 20px;
      /* width: 10%; */
    }

    @keyframes animated-text {
      from {
        width: 0;
      }
      to {
        width: 350px;
      }
    }
  }
  @media (min-width: 300px) and (max-width: 349px) {
    h1 {
      font-size: 24px;
    }
    p {
      font-size: 18px;
      /* width: 10%; */
    }

    @keyframes animated-text {
      from {
        width: 0;
      }
      to {
        width: 220px;
      }
    }
  }
  @media (min-width: 280px) and (max-width: 299px) {
    h1 {
      font-size: 24px;
    }
    p {
      font-size: 18px;
      /* width: 10%; */
    }

    @keyframes animated-text {
      from {
        width: 0;
      }
      to {
        width: 220px;
      }
    }
  }
</style>
