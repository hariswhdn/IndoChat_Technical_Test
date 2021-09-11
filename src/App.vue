<template>
  <div className="navbar">
    <div>
      <i className="material-icons">menu</i>
      <a href="#">
        <img src="./assets/images/logo.png" alt="logo" />
      </a>
      <div>
        <div>
          <a href="#" className="active">Home</a>
          <a href="#discover">Discover</a>
          <a href="#auth">Register</a>
        </div>
        <div>
          <a href="#search">
            <i className="material-icons">search</i>
          </a>
        </div>
      </div>
    </div>
    <ul className="d_none">
      <li>
        <a href="#" className="active">Home</a>
      </li>
      <li>
        <a href="#discover">Discover</a>
      </li>
      <li>
        <a href="#auth">Register</a>
      </li>
    </ul>
  </div>
  <div className="banner">
    <div>
      <img src="./assets/images/a.jpg" alt="./assets/images" />
      <div>
        <p className="card_text">
          <span className="display_2 font_weight_bold">Booked Tool </span
          >enables you to create Interactive Advertisement
        </p>
        <input
          type="button"
          value="What is it?"
          onclick="window.location='#discover';"
        />
      </div>
    </div>
    <div>
      <img src="./assets/images/b.jpg" alt="./assets/images" />
    </div>
  </div>
  <div id="auth" className="auth">
    <p className="card_text">
      Please log in to start using<br /><span
        className="display_1 font_weight_bold"
        >Booked Tool</span
      >
    </p>
    <form action="#auth">
      <input type="email" placeholder="Email" />
      <input type="password" placeholder="Password" />
      <input type="submit" value="Login" />
    </form>
  </div>
  <div id="discover" className="card">
    <div className="tab">
      <div className="card_header">
        <i className="material-icons">insights</i>
        <span className="font_weight_bold display_2">DISCOVER</span>
        <span className="display_2">BOOKED TOOL</span>
      </div>
      <div>
        <img src="./assets/images/c.jpg" alt="./assets/images" />
        <img
          className="d_none"
          src="./assets/images/c.jpg"
          alt="./assets/images"
        />
        <img
          className="d_none"
          src="./assets/images/c.jpg"
          alt="./assets/images"
        />
        <img
          className="d_none"
          src="./assets/images/c.jpg"
          alt="./assets/images"
        />
      </div>
      <div>
        <ul className="display_3">
          <li className="active">
            <span>Discover A</span>
          </li>
          <li>
            <span>Discover B</span>
          </li>
          <li>
            <span>Discover C</span>
          </li>
          <li>
            <span>Discover D</span>
          </li>
        </ul>
        <div>
          <p>
            A Lorem ipsum dolor sit amet consectetur, adipisicing elit. Amet
            corporis quo, consectetur aspernatur quos minus ipsam neque beatae
            repellat iste voluptate quaerat esse, deserunt vero magni fuga
            fugit vel. Eligendi.
          </p>
          <p className="d_none">
            B Lorem ipsum dolor sit amet consectetur, adipisicing elit. Amet
            corporis quo, consectetur aspernatur quos minus ipsam neque beatae
            repellat iste voluptate quaerat esse, deserunt vero magni fuga
            fugit vel. Eligendi.
          </p>
          <p className="d_none">
            C Lorem ipsum dolor sit amet consectetur, adipisicing elit. Amet
            corporis quo, consectetur aspernatur quos minus ipsam neque beatae
            repellat iste voluptate quaerat esse, deserunt vero magni fuga
            fugit vel. Eligendi.
          </p>
          <p className="d_none">
            D Lorem ipsum dolor sit amet consectetur, adipisicing elit. Amet
            corporis quo, consectetur aspernatur quos minus ipsam neque beatae
            repellat iste voluptate quaerat esse, deserunt vero magni fuga
            fugit vel. Eligendi.
          </p>
        </div>
      </div>
    </div>
  </div>
  <div className="card">
    <div className="contact">
      <div className="card_header">
        <i className="material-icons">pages</i>
        <span className="font_weight_bold display_2">Get in touch</span>
        <span className="display_4"
          >Want to get in touch? We'd love to hear from you. Here's how you
          can reach us..</span
        >
      </div>
      <div className="search">
        <label className="material-icons" for="search">search</label>
        <input type="text" id="search" placeholder="Search..." />
      </div>
      <div>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d991.6564564982963!2d106.8253891985585!3d-6.180810107869931!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f42c022144c3%3A0xfe6941ee5d3ab9d8!2sWisma%20Antara%2C%20Jl.%20Medan%20Merdeka%20Sel.%20No.17%2C%20RT.11%2FRW.2%2C%20Gambir%2C%20Kecamatan%20Gambir%2C%20Kota%20Jakarta%20Pusat%2C%20Daerah%20Khusus%20Ibukota%20Jakarta%2010110!5e0!3m2!1sen!2sid!4v1631273783665!5m2!1sen!2sid"
          width="600"
          height="450"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
        <form action="#">
          <span className="display_2 font_weight_bold">Feedback</span>
          <div>
            <input type="text" placeholder="First" />
            <input type="text" placeholder="Last" />
          </div>
          <input type="email" placeholder="Email" />
          <textarea placeholder="Message" rows="7"></textarea>
          <input type="submit" value="Send" />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
global.jQuery = require("jquery");
var $ = global.jQuery;
window.$ = $;
$(function () {
  $(".container > .navbar > div > i").click(function () {
    $(".container > .navbar > ul").toggleClass("d_none");
  });
  $("#discover > .tab > div:last-child > ul > li").click(function () {
    if (!$(this).hasClass("active")) {
      $(
        "#discover > .tab > div:nth-child(2), #discover > .tab > div:last-child > div"
      ).css("opacity", 0);
      let index = $(this).index() + 1;
      $(
        "#discover > .tab > div:nth-child(2) > img:not(.d_none), #discover > .tab > div:last-child > div > p:not(.d_none)"
      ).addClass("d_none");
      $(
        "#discover > .tab > div:nth-child(2) > img:nth-child(" +
          index +
          "), #discover > .tab > div:last-child > div > p:nth-child(" +
          index +
          ")"
      ).removeClass("d_none");
      $("#discover > .tab > div:last-child > ul > li.active").removeClass(
        "active"
      );
      $(
        "#discover > .tab > div:last-child > ul > li:nth-child(" + index + ")"
      ).addClass("active");
      $(
        "#discover > .tab > div:nth-child(2), #discover > .tab > div:last-child > div"
      ).fadeTo(250, 1);
    }
  });
});
</script>


<style lang="scss">
@import "./assets/css/normalize.css";
@font-face {
  font-family: "Roboto";
  font-weight: 300;
  src: url("./assets/fonts/Roboto-Light.ttf");
}
@font-face {
  font-family: "Roboto";
  font-weight: 400;
  src: url("./assets/fonts/Roboto-Regular.ttf");
}
@font-face {
  font-family: "Roboto";
  font-weight: 700;
  src: url("./assets/fonts/Roboto-Bold.ttf");
}
@font-face {
  font-family: "Material Icons";
  font-style: normal;
  font-weight: 400;
  src: local("Material Icons"), local("MaterialIcons-Regular"),
    url("./assets/fonts/MaterialIcons-Regular.ttf") format("truetype");
}
/**/
$primary1: #fdfefe;
$primary2: #f3f6f4;
$primary3: #f6f8f8;
$primary4: #e0e1e0;
$primary5: #e2e3e2;
$primary6: #ccc9c8;
$primary7: #ffffff;
$accent: #428ecb;
$neutral1: rgba(0, 0, 0, 0.05);
$neutral2: rgba(0, 0, 0, 0.375);
$neutral3: rgba(0, 0, 0, 0.625);
$neutral4: rgba(0, 0, 0, 0.75);
$neutral5: rgba(0, 0, 0, 0.875);
$neutral6: rgba(255, 255, 255, 0.875);
/**/
body {
  color: $neutral4;
  font-family: "Roboto", sans-serif;
  font-size: 18px;
  a {
    color: $neutral4;
    text-decoration: none;
  }
  input {
    padding: 18px 28px;
    color: $neutral3;
    font-size: 20px;
    border: 0;
    border-radius: 4px;
    &:focus {
      outline: none;
    }
    &::placeholder {
      color: $neutral2;
    }
    &[type="button"],
    &[type="submit"] {
      background-color: $accent;
      color: $neutral6;
      font-size: 18px;
      border-radius: 8px;
      &:hover {
        cursor: pointer;
      }
    }
  }
  p {
    margin: 0;
  }
  textarea {
    resize: none;
    &:focus {
      outline: none;
    }
    &::placeholder {
      color: $neutral2;
    }
  }
  ul {
    margin: 0;
    padding-left: 0;
    display: flex;
    list-style: none;
  }
}
/**/
.container {
  background-color: $primary2;
  max-width: 1440px;
  margin: 0 auto;
  /**/
  .material-icons {
    font-family: "Material Icons";
    font-weight: normal;
    font-style: normal;
    font-size: 24px;
    display: inline-block;
    line-height: 1;
    text-transform: none;
    letter-spacing: normal;
    word-wrap: normal;
    white-space: nowrap;
    direction: ltr;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    -moz-osx-font-smoothing: grayscale;
    font-feature-settings: "liga";
  }
  .display_1 {
    font-size: 36px;
  }
  .display_2 {
    font-size: 28px;
  }
  .display_3 {
    font-size: 26px;
  }
  .display_4 {
    font-size: 22px;
  }
  .font_weight_bold {
    font-weight: 700;
  }
  .card_header {
    margin-bottom: 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    line-height: 40px;
  }
  .card_text {
    font-size: 20px;
    line-height: 30px;
  }
  .card_header {
    > .material-icons {
      margin-bottom: 10px;
      font-size: 48px;
    }
    > span {
      &:last-child {
        color: $neutral3;
      }
    }
  }
  .d_none {
    display: none !important;
  }
  /**/
  > .navbar {
    background-color: $primary3;
    padding: 6px 36px;
    > div {
      display: flex;
      align-items: center;
      justify-content: space-between;
      > a {
        background-color: $primary7;
        width: 56px;
        height: 56px;
        margin-bottom: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        box-shadow: 0 4px $primary6;
        > img {
          height: 30px;
        }
      }
      > div {
        display: flex;
        align-items: center;
        > div {
          &:first-child {
            display: flex;
            > a {
              padding: 10px 48px;
              &.active {
                background-color: $primary4;
                border-radius: 38px;
              }
            }
          }
          &:last-child {
            > a {
              padding: 10px;
              display: flex;
              align-items: center;
            }
          }
        }
      }
      > i {
        padding: 10px;
        display: none;
        cursor: pointer;
      }
    }
    > ul {
      display: flex;
      flex-direction: column;
      > li {
        display: flex;
        > a {
          width: 100%;
          padding: 10px 14px;
        }
      }
    }
  }
  > .banner {
    display: flex;
    > div {
      width: 50%;
      &:first-child {
        width: calc(50% + 50px);
        display: flex;
        position: relative;
        > div {
          position: absolute;
          top: calc(50% - 70px);
          left: calc(50% - 35px);
          right: 50px;
          transform: translateY(-50%);
          > p {
            margin-bottom: 10px;
          }
        }
      }
      &:last-child {
        width: 50%;
        margin-left: -50px;
        z-index: 1;
      }
      > img {
        width: 100%;
      }
    }
  }
  > .auth {
    background-color: $primary5;
    padding: 64px 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    > .card_text {
      margin-right: 56px;
    }
    > form {
      display: flex;
      > input {
        &[type="submit"] {
          padding-right: 32px;
          padding-left: 32px;
        }
        &:not(:first-child):not(:last-child) {
          margin-left: 20px;
        }
        &:last-child {
          margin-left: 28px;
        }
      }
    }
  }
  > .card {
    padding: 48px 36px;
    display: flex;
    align-items: center;
    flex-direction: column;
    &:nth-child(even) {
      background-color: $primary1;
    }
    &:nth-child(odd) {
      background-color: $primary3;
    }
    > .tab {
      width: calc(60% - 40px);
      > div {
        display: flex;
        flex-direction: column;
        align-items: center;
        &:nth-child(2) {
          > img {
            width: calc(100% - 150px);
            border-radius: 8px;
          }
        }
        &:nth-child(3) {
          > ul {
            margin: 26px 0;
            width: 100%;
            justify-content: center;
            border-bottom: 2px solid $primary5;
            > li {
              padding: 0 28px;
              display: flex;
              &:hover {
                cursor: pointer;
              }
              &.active {
                > span {
                  font-weight: 700;
                  border-color: $accent;
                  transition: all 0.5s ease;
                }
              }
              > span {
                padding: 4px 0;
                border-bottom: 8px solid transparent;
              }
            }
          }
          div {
            display: flex;
            justify-content: center;
            > p {
              width: calc(100% - 100px);
              font-size: 20px;
              line-height: 30px;
            }
          }
        }
      }
    }
    > .contact {
      width: calc(60% - 40px);
      display: flex;
      flex-direction: column;
      align-items: center;
      > .search {
        background-color: $primary7;
        width: 100%;
        display: flex;
        align-items: center;
        border-radius: 4px;
        > .material-icons {
          padding-left: 20px;
        }
        > input[type="text"] {
          width: 100%;
          padding-left: 20px;
        }
      }
      > div:last-child {
        width: 100%;
        display: flex;
        margin-top: 30px;
        > iframe {
          width: 50%;
        }
        > form {
          width: calc(50% - 72px);
          padding: 24px 36px;
          background-color: $primary7;
          > span {
            display: inline-block;
            margin-bottom: 20px;
          }
          > div {
            display: flex;
            > input {
              padding: 10px;
              border: 1px solid $neutral1;
              &:first-child {
                width: calc(40% - 5px);
              }
              &:last-child {
                width: calc(60% - 5px);
              }
              &:not(:last-child) {
                margin-right: 10px;
              }
            }
          }
          > textarea {
            border-radius: 4px;
          }
          > input:not([type="submit"]),
          > textarea {
            width: calc(100% - 20px);
            padding: 10px;
            border: 1px solid $neutral1;
          }
          > *:not(span):not(:last-child) {
            margin-bottom: 10px;
          }
        }
      }
    }
  }
}
@media (min-width: 992px) {
  .container > .navbar > ul {
    display: none;
  }
}
@media (max-width: 1439.98px) {
  .container > .banner > div {
    width: 100%;
  }
  .container > .banner > div:first-child {
    width: 100%;
    height: 300px;
    justify-content: center;
    overflow: hidden;
  }
  .container > .banner > div:first-child > img {
    position: absolute;
    top: calc(50%);
    left: calc(50%);
    transform: translate(-50%, -50%);
    opacity: 0.375;
  }
  .container > .banner > div:first-child > div {
    margin: 0 24px;
    position: absolute;
    top: calc(50%);
    left: unset;
    right: unset;
  }
  .container > .banner > div:last-child {
    display: none;
  }
  .container > .card > .contact,
  .container > .card > .tab {
    width: 100%;
  }
  .container
    > .card
    > .contact
    > div:last-child
    > form
    > div
    > input:first-child,
  .container
    > .card
    > .contact
    > div:last-child
    > form
    > div
    > input:last-child {
    width: calc(50% - 5px);
  }
  .container > .card > .contact > div:last-child > form > input[type="submit"] {
    width: 100%;
  }
}
@media (max-width: 1199.98px) {
  .container > .auth {
    flex-direction: column;
    padding: 36px 24px;
  }
  .container > .auth > .card_text {
    margin: 0 0 24px 0;
  }
  .container > .auth > form {
    width: 100%;
  }
  .container > .auth > form > input:not([type="submit"]) {
    width: 40%;
  }
  .container > .auth > form > input[type="submit"] {
    width: 20%;
  }
  .container > .auth > form > input:not(:first-child):not(:last-child) {
    margin-left: 24px;
  }
  .container > .auth > form > input:last-child {
    margin-left: 24px;
  }
}
@media (max-width: 991.98px) {
  .container > .card > .contact > div:last-child > form > div {
    flex-direction: column;
  }
  .container
    > .card
    > .contact
    > div:last-child
    > form
    > div
    > input:first-child,
  .container
    > .card
    > .contact
    > div:last-child
    > form
    > div
    > input:last-child {
    width: unset;
  }
  .container
    > .card
    > .contact
    > div:last-child
    > form
    > div
    > input:not(:last-child) {
    margin-right: 0;
    margin-bottom: 10px;
  }
  .container > .card > .tab > div:nth-child(2) > img {
    width: 100%;
  }
  .container > .card > .tab > div:nth-child(3) div > p {
    width: unset;
  }
  .container > .card > .tab > div:nth-child(3) {
    margin-top: 24px;
    flex-direction: row;
    align-items: flex-start;
  }
  .container > .card > .tab > div:nth-child(3) > ul {
    width: unset;
    margin: 0 36px 0 0;
    flex-direction: column;
    border: 0;
  }
  .container > .card > .tab > div:nth-child(3) > ul > li {
    padding: 6px 0;
  }
  .container > .card > .tab > div:nth-child(3) > ul > li > span {
    white-space: nowrap;
  }
  .container > .card > .tab > div:nth-child(3) div {
    padding-top: 6px;
  }
}
@media (max-width: 767.98px) {
  .container > .navbar {
    padding-right: 14px;
    padding-left: 14px;
  }
  .container > .navbar > div > i {
    display: block;
  }
  .container > .navbar > div > div > div:first-child {
    display: none;
  }
  .container > .auth > form {
    display: flex;
    flex-direction: column;
  }
  .container > .auth > form > input:not([type="submit"]) {
    margin-bottom: 18px;
  }
  .container > .auth > form > input:not([type="submit"]),
  .container > .auth > form > input[type="submit"] {
    width: unset;
  }
  .container > .auth > form > input:not(:first-child):not(:last-child),
  .container > .auth > form > input:last-child {
    margin-left: 0;
  }
  .container > .card {
    padding: 36px 24px;
  }
  .container > .card > .contact > div:last-child {
    flex-direction: column;
    margin-top: 18px;
  }
  .container > .card > .contact > div:last-child > iframe {
    width: 100%;
  }
  .container > .card > .contact > div:last-child > form {
    width: calc(100% - 72px);
    margin-top: 18px;
  }
  .container > .card > .contact > div:last-child > iframe,
  .container > .card > .contact > div:last-child > form {
    border-radius: 4px;
  }
}
</style>
