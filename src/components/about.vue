<template>
  <section class="about" id="about">
    <header class="header flex justify-between items-center flex-wrap gap-y-5">
      <div class="header__logo flex items-center gap-x-3 cursor-pointer">
        <img src="../img/Logo.png" alt="Logo" />
        <span class="text-xl font-black"
          >Lasles<span style="font-weight: 700">VPN</span></span
        >
      </div>
      <ul class="header__list flex align-center gap-x-14 flex-wrap">
        <li class="header__li" v-for="list in lists" :key="list.id">
          <a :href="list.href" class="header__link text-stand font-bold">{{
            list.name
          }}</a>
        </li>
      </ul>
      <div class="header__sign flex items-center gap-x-7">
        <a class="header__signIn font-black text-xl cursor-pointer">Sign In</a>
        <my-select>Sign Up</my-select>
      </div>
    </header>
    <div class="about__banner flex my-9 items-center gap-x-4">
      <div class="about__banner-inf flex flex-col gap-y-7">
        <h1 class="text-6xl">
          Want anything to be easy with
          <strong class="font-bold">LaslesVPN.</strong>
        </h1>
        <p class="max-w-xl">
          Provide a network for all your needs with ease and fun using LaslesVPN
          discover interesting features from us.
        </p>
        <my-button class="my-3">get started</my-button>
      </div>
      <div class="about__banner-picture">
        <img src="../img/about.png" alt="About picture" />
      </div>
    </div>
    <div class="about__footer flex items-center justify-center">
      <div class="about__footer-items flex justify-between">
        <div class="about__footer-item">
          <img src="../img/user.png" alt="User" />
          <div>
            <h2>90+</h2>
            <time>Users</time>
          </div>
        </div>
        <div class="about__footer-item">
          <img src="../img/location.png" alt="Location" />
          <div>
            <h2>30+</h2>
            <time>Locations</time>
          </div>
        </div>
        <div class="about__footer-item">
          <img src="../img/server.png" alt="Server" />
          <div>
            <h2>50+</h2>
            <time>Servers</time>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "about",
  data() {
    return {
      lists: [
        {
          name: "About",
          id: 1,
          href: "#about",
        },
        {
          name: "Features",
          href: "#feature",
          id: 2,
        },
        {
          name: "Pricing",
          href: "#customer",
          id: 3,
        },
        {
          name: "Testimonials",
          href: "#customer",
          id: 4,
        },
        {
          name: "Help",
          href: "#footer",
          id: 5,
        },
      ],
    };
  },
};
</script>
<style scoped>
.header__li a {
  font-size: 20px;
}
.header__signUp {
  border: 1px solid #f53855;
  border-radius: 50px;
  color: #f53855;
  width: 150px;
  text-align: center;
  cursor: pointer;
}
.header__signIn:hover {
  color: purple;
}
.header__signUp:hover {
  background-color: #f53855;
  border: none;
  transition: 1s;
  color: #fff;
}
.header__link:hover {
  color: #111;
  transition: 0.5s;
}
.about__banner-inf h1 {
  line-height: 87px;
}
.about__banner-inf {
  width: 82%;
}
.about__banner-picture img {
  height: 382px;
  width: 611px;
  object-fit: cover;
}
.about__footer {
  position: relative;
  height: 200px;
  margin-top: 85px;
  border-radius: 10px;
  box-shadow: 1px 1px 2px 2px #e5e5e5;
}

.about__footer-items {
  width: 85%;
}
.about__footer-item {
  position: relative;
  align-items: center;
  gap: 28px;
  display: flex;
}
.about__footer-item div h2 {
  font-weight: bold;
  font-size: 20px;
}
.about__footer-items .about__footer-item:first-child::after {
  display: none;
}
.about__footer-item::after {
  content: "";
  position: absolute;
  height: 126px;
  right: 0;
  margin-right: 273px;
  width: 1px;
  border: 2px solid #eeeff2;
}
.header__signIn {
  color: #0b132a;
}

@media screen and (max-width: 1040px) {
  .about__footer-item::after {
    display: none;
  }
  .header__list {
    gap: 30px;
  }
}
@media screen and (max-width: 750px) {
  .about__banner-picture {
    display: none;
  }
}
@media screen and (max-width: 620px) {
  .about__footer-items {
    flex-wrap: wrap;
    gap: 13px;
  }
}
@media screen and (max-width: 380px) {
  .about__banner-inf h1 {
    font-size: 2rem;
    line-height: 1.5;
  }
}
@media screen and (max-width: 340px) {
  .about__banner-inf {
    text-align: center;
  }
  .about__banner-inf .btn {
    width: 80%;
    margin: auto;
  }
  .header__sign {
    flex-direction: column;
  }
}
</style>
