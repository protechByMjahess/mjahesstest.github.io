<script>
  import { Router, Link, Route } from "svelte-routing";
  //   import { Link } from "svelte-routing";

  import Nested from "./routes/About.svelte";
  // import FeedbackList from "./routes/NotFound.svelte";
  import FeedbackList from "./routes/Homme.svelte";
  import Achievments from "./routes/achievments.svelte";
  import Experience from "./routes/Experience.svelte";
  // hello
  let toggle = true;
  let change = () => {
    if (!toggle) toggle = !toggle;
    return toggle;
  };

  //   hhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh
  import { onMount } from "svelte";

  let indicator;
  let navItems = [];

  function handleClick(event) {
    const clickedItem = event.currentTarget;
    const leftDistance = clickedItem.getBoundingClientRect().left;
    const elementWidth = clickedItem.offsetWidth;

    navItems.forEach((item) => {
      item.classList.remove("is-active");
    });
    clickedItem.classList.add("is-active");

    indicator.style.backgroundColor = clickedItem.dataset.color;
    indicator.style.width = `${elementWidth}px`;
    indicator.style.left = `${leftDistance}px`;
  }

  onMount(() => {
    indicator = document.querySelector(".movable-indicator");
    navItems = Array.from(document.querySelectorAll(".nav-i"));
    navItems.forEach((item) => {
      item.addEventListener("click", handleClick);
    });
  });
</script>

<div class="app">
  <Router>
    <!-- <nav>
		<Link to="/">Home</Link>
		<Link to="/aboutt" on:click={change}>About</Link>
	  </nav> -->
    <!--  Navbar  -->
    <div class="mb-5 mt-5 px-3">
      <nav class="nav nnav">
        <span>
          <Link
            style="text-decoration:none;color:rgb(0, 217, 255);"
            class="nav-i link about-me"
            data-color="rgb(0, 217, 255)"
            to="/">About Me</Link
          >
        </span>
        <span>
          <Link
            style="text-decoration:none;color:lime"
            class="nav-i link skills"
            to="/aboutt"
            data-color="lime"
            on:click={change}>Skills</Link
          >
        </span>
        <span>
          <Link
            style="text-decoration:none;color:lime"
            class="nav-i  link achievements"
            to="/achievments"
            data-color="lime"
            on:click={change}>Achievments</Link
          >
        </span>
        <span>
          <Link
            style="text-decoration:none;color:lime"
            class="nav-i link experience"
            to="/experience"
            data-color="lime"
            on:click={change}>Experience</Link
          >
        </span>

        <!-- <span class="movable-indicator" /> -->
        <span class="movable-indicator" />
      </nav>
    </div>

    <Route path="/" component={FeedbackList} />
    <Route path="/aboutt" component={Nested} />
    <Route path="/achievments" component={Achievments} />
    <Route path="/experience" component={Experience} />
  </Router>

  <!-- footer footer   footer footer   footer footer footer footer footer footer footer footer footer footer footer footer -->
  <!-- Site footer -->
  <!-- <div class="footer-wrapper" /> -->
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-address">
        <h4 style="color:lime;">Address</h4>
        <p style="color:rgb(0, 217, 255);">Mazraat Yachou3</p>
      </div>
      <div class="footer-contact">
        <h4 style="color:lime;">Contact Me</h4>
        <p style="color:rgb(0, 217, 255);">Phone: +961 76 155 955</p>
        <p style="color:rgb(0, 217, 255);">Email: jjadsalamehh@gmail.com</p>
      </div>
      <div class="footer-form">
        <h4 style="color:lime;">Any Question?</h4>
        <form>
          <input
            style="background-color: #2d2c2c; color:lime;"
            type="text"
            placeholder="Name"
            required
          />
          <input
            style="background-color: #2d2c2c; color:lime;"
            type="email"
            placeholder="Email"
            required
          />
          <textarea
            style="background-color: #2d2c2c; color:lime;"
            placeholder="Message"
            required
          />
          <button type="submit" style="color:lime;border: 1px solid lime;"
            >Send</button
          >
        </form>
      </div>
    </div>
    <div class="footer-bottom" style="border-top:2px solid rgb(0, 217, 255);">
      <p style="color:lime;">
        &copy; 2023 Salameh Portfolio. All rights reserved.
      </p>
    </div>
  </footer>
</div>

<!-- Site footer -->

<style>
  /* .about-me {
		color: rgb(0, 217, 255) !important;
	  }
	
	  .skills {
		color: lime !important;
	  }
	
	  .achievements {
		color: lime !important;
	  }
	
	  .experience {
		color: lime !important;
	  } */

  /* nnnnnnnnnnnnnnn */
  input::placeholder {
    color: rgb(0, 217, 255);
    /* color: #2d2c2c; */
    /* Additional styles for the placeholder */
  }
  textarea::placeholder {
    color: rgb(0, 217, 255);
    /* Additional styles for the placeholder */
  }

  /*  */
  input:focus::placeholder,
  textarea:focus::placeholder {
    color: transparent; /* Make the placeholder text transparent */
  }
  .nnav {
    background-image: url(laptop.jpg);
    background-size: cover;
    background-position: center;
    height: 60px;
  }
  .app {
    background-image: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/1462889/pat-back.svg");

    /* background-position: center; */
    background-repeat: repeat;
    background-size: 4%;
  }
  * {
    background-image: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/1462889/pat-back.svg");
    background-size: 40%;

    /* background-position: center;
		background-repeat: repeat;
		background-size: 4%; */
  }
  ::-webkit-scrollbar {
    display: none;
  }
  @import "bootstrap/dist/css/bootstrap.min.css";

  /* Navbar styling */
  .nav {
    margin: -8px;
    display: flex;
    justify-content: space-evenly;
    position: relative;
    overflow: hidden;
    background-color: black;
    color: rgb(0, 217, 255);
    padding: 0 20px;
    box-shadow: 0 5px 10px 0px rgb(235, 233, 233);
  }

  /* Link styling */
  span {
    font-size: 40px;
  }
  span:hover {
    text-decoration: none;
  }
  /* .nav-i:hover {
		text-decoration: none;
	  } */

  /* Movable indicator styling */
  .movable-indicator {
    position: absolute;
    content: "";
    bottom: 0;
    left: 0;
    width: 100%;
    height: 5px;
    background-color: rgb(0, 217, 255);
    border-radius: 5px;
    transition: 0.62s cubic-bezier(0.23, 0.55, 0.42, 1.51) all;
  }

  /* footer footer  footer footer  footer footer  footer footer  footer footer  footer footer  footer footer */

  .footer {
    background-color: black;
    padding: 20px;
    margin: -8px;
  }

  .footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-gap: 20px;
  }

  .footer h4 {
    font-size: 18px;
    margin-bottom: 10px;
    color: #333;
  }

  .footer p {
    font-size: 14px;
    margin-bottom: 5px;
    color: #555;
  }

  .footer-form input,
  .footer-form textarea {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid rgb(0, 217, 255);
    border-radius: 4px;
  }
  .footer-form input:focus,
  .footer-form textarea:focus {
    outline: 2px solid lime;
    border-color: transparent;
  }

  .footer-form button {
    background-color: #2d2c2c;
    /* color: #fff; */
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  .footer-form button:hover {
    background-color: #333;
  }

  .footer-bottom {
    margin-top: 20px;
    text-align: center;
    font-size: 12px;
    color: #777;
  }

  @media (min-width: 700px) and (max-width: 937px) {
    span {
      font-size: 32px;
    }
    .nav {
      height: 50px;
    }
  }
  @media (min-width: 500px) and (max-width: 699px) {
    span {
      font-size: 23px;
    }
    .nav {
      height: 41px;
    }
  }
  @media (min-width: 400px) and (max-width: 499px) {
    span {
      font-size: 18px;
    }
    .nav {
      height: 41px;
    }
  }
  @media (min-width: 350px) and (max-width: 399px) {
    span {
      font-size: 16px;
    }
    .nav {
      height: 35px;
      display: flex;
      justify-content: space-between;
    }
  }
  @media (min-width: 300px) and (max-width: 349px) {
    span {
      font-size: 13px;
    }
    .nav {
      height: 27px;
      display: flex;
      justify-content: space-between;
    }
  }
  @media (max-width: 327px) {
    input,
    textarea {
      width: 250px !important;
    }
  }
  @media (min-width: 280px) and (max-width: 299px) {
    span {
      font-size: 11px;
    }
    .nav {
      height: 27px;
      display: flex;
      justify-content: space-between;
    }
  }
</style>
