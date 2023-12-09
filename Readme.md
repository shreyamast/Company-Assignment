/* Global Css */
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;600;700&family=Rubik:wght@400;500;600;700&display=swap");

*,
::after,
::before {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
  font-family: "Oswald", sans-serif;
}

:root {
  --black: #212529;
  --white: #fff;
  --button-pink: #ffbfcb;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
  color: var(--black);
}

/* common css */
.flex {
  display: flex;
}

h1,
h2,
h3 {
  font-weight: 600;
  letter-spacing: 3px;
  color: var(--white);
}

h1 {
  font-size: 3.2rem;
  text-transform: uppercase;
}

h2 {
  font-size: 2.8rem;
}

h3 {
  font-size: 2.4rem;
}

/* navbar styling */
header a {
  font-size: 2.2rem;
}

.navbar {
  background-color: var(--white);
  padding: 1rem 0;
}

.hamburger {
  width: 3.6rem;
  height: 3.6rem;
  display: none;
}

.menu {
  flex: 0 1 140rem;
}

.menu-bar {
  justify-content: space-evenly;
  display: none;
}

input[type="checkbox"] {
  display: none;
}

input[type="checkbox"]:checked ~ .menu-bar {
  display: flex;
  flex-direction: column;
}

.menu_item {
  display: grid;
  place-items: center;
}

.social-icons {
  flex: 1 1 auto;
  margin-right: 2rem;
}

.social-icons ul {
  gap: 1.6rem;
  justify-content: center;
}

.featured-icon {
  width: 2.2rem;
  height: 2.2rem;
}

@media (min-width: 821px) {
  .menu-bar {
    display: flex ;
    flex-direction: row ;
  }
}

@media (max-width: 51.25em) {
  html {
    font-size: 50%;
  }

  .menu {
    flex: 1 1 auto;
    position: relative;
  }

  .menu-bar {
    gap: 1.5rem;
    padding: 1rem 0;
    position: absolute;
    z-index: 1;
    top: 4.5rem;
    left: 0;
    width: 25rem;
    background: linear-gradient(
      to right,
      rgba(255, 135, 167, 1) 10%,
      rgba(255, 203, 105, 1) 100%
    );
  }

  .hamburger {
    display: block;
    margin-left: 2rem;
  }

  .social-icons ul {
    margin-right: 2rem;
    justify-content: right;
  }
}

/* styling for hero section */
.hero {
  background: url(./img/hero-banner.png);
  background-position: center;
  background-size: cover;
  height: 45rem;
  position: relative;
}

.hero-about {
  background-color: rgba(222, 125, 136, 0.8);
  width: 50rem;
  padding: 5rem;
  color: var(--white);
  position: absolute;
  top: 5rem;
  left: 8rem;
}

.hero-about p {
  font-size: 1.4rem;
  font-weight: 100;
  letter-spacing: 2px;
}

@media (max-width: 32.5em) {
  h1 {
    font-size: 2.8rem;
  }

  .hero-about {
    left: 5%;
    width: 90%;
  }

  .hero-about p {
    font-size: 1.2rem;
  }
}

/* styling for card section */
.cards {
  background: linear-gradient(
    to right,
    rgba(255, 135, 167, 1) 10%,
    rgba(255, 203, 105, 1) 100%
  );
  padding: 4.2rem 0 2.6rem;
}

.box {
  margin: 0 auto;
  width: 80%;
}

.box-content {
  justify-content: space-evenly;
}

.heading-secondary {
  text-align: center;
  margin-bottom: 5.2rem;
}

.card {
  border: 10px solid #fff;
  max-width: 20rem;
  border-radius: 0 18%;
  overflow: hidden;
}

.card-img {
  width: 100%;
  height: 18rem;
}

.card-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-text {
  background-color: #fff;
  text-align: center;
}

@media (max-width: 51.25em) {
  .cards .heading-tertiary {
    font-size: 1.8rem;
  }

  .card-text p {
    font-size: 1.2rem;
  }
}

.heading-tertiary {
  color: var(--black);
}

.box {
  text-align: center;
}

.box button {
  margin-top: 4.2rem;
  color: var(--black);
  border-radius: 20px;
  padding: 1rem 3rem;
  outline: none;
  border: none;
  background: rgb(248, 203, 211);
  font-weight: 600;
}

@media (max-width: 43.75em) {
  .box-content {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }

  .card {
    max-width: 25rem;
  }
}
