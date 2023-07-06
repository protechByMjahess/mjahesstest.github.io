<div class="h1">
  <h1>Winner of local robotics competition:</h1>
</div>
<div class="container">
  <div class="content">
    <p>
      Creation of an RFID car lock and alarm system that was installed on a car.
    </p>
  </div>
</div>
<div class="h1">
  <h1>PetSocial APP:</h1>
</div>
<div class="container">
  <div class="content">
    <p>
      Creation of a social media application for pets that was presented as my
      final project
    </p>
  </div>
</div>
<div class="h1">
  <h1>Winner of the NEEDS SOrCE platform competition hosted at ccj</h1>
  <h1>Competitor at the Lebanese collegiate programming contest (LCPC)</h1>
</div>

<style>
  .h1 {
    text-align: center;
  }
  .container {
    /* background-color: green; */
    display: flex;
    justify-content: center;
    align-items: center;
    /* text-align: center; */

    /* height: 100vh; */
  }
  .content {
    text-align: center;
  }

  p {
    font-size: 28px;
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
  /* jjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjj */
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
