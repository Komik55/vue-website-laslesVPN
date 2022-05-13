<template>
  <section class="features" id="feature">
    <div class="features__inf flex items-end justify-between gap-x-9">
      <div class="features__inf-picture">
        <img src="../img/features.png" alt="Picture" />
      </div>
      <div class="features__inf-sec">
        <h2 class="text-5xl max-w-lg leading-21">
          We Provide Many Features You Can Use
        </h2>
        <p class="max-w-sm text-medium my-8">
          You can explore the features that we provide with fun and have their
          own functions each feature.
        </p>
        <ul class="features__list">
          <li>Powerfull online protection.</li>
          <li>Internet without borders.</li>
          <li>Supercharged VPN</li>
          <li>No specific time limits.</li>
        </ul>
      </div>
    </div>
    <div class="plan flex flex-col items-center py-5 gap-y-9">
      <div class="plan__inf text-center">
        <h2 class="font-bold text-2xl mb-4">Choose Your Plan</h2>
        <p class="max-w-xl">
          Let's choose the package that is best for you and explore it happily
          and cheerfully.
        </p>
      </div>
      <div class="plan__items flex gap-x-9 justify-between">
        <div class="plan__item items-center">
          <div>
            <img src="../img/Free.png" alt="Free" />
            <h2 class="font-bold text-lg">Free Plan</h2>
            <ul class="plan__list">
              <li>Unlimited Bandwitch</li>
              <li>Encrypted Connection</li>
              <li>No Traffic Logs</li>
              <li>Works on All Devices</li>
            </ul>
            <div class="plan__select" style="margin-top: 150px">
              <h2 class="font-bold">Free</h2>
              <my-select>Select</my-select>
            </div>
          </div>
        </div>

        <div class="plan__item">
          <div>
            <img src="../img/Free.png" alt="Free" />
            <h2 class="font-bold text-lg">Standard Plan</h2>
            <ul class="plan__list">
              <li>Unlimited Bandwitch</li>
              <li>Encrypted Connection</li>
              <li>Yes Traffic Logs</li>
              <li>Works on All Devices</li>
              <li>Connect Anyware</li>
            </ul>
            <div class="plan__select" style="margin-top: 110px">
              <h2><strong>$9</strong> / mo</h2>
              <my-select>Select</my-select>
            </div>
          </div>
        </div>

        <div class="plan__item">
          <div>
            <img src="../img/Free.png" alt="Free" />
            <h2 class="font-bold text-lg">Premium Plan</h2>
            <ul class="plan__list">
              <li>Unlimited Bandwitch</li>
              <li>Encrypted Connection</li>
              <li>Yes Traffic Logs</li>
              <li>Works on All Devices</li>
              <li>Connect Anyware</li>
              <li>Get New Features</li>
            </ul>
            <div class="plan__select" style="margin-top: 70px">
              <h2><strong>$12</strong> / mo</h2>
              <my-select>Select</my-select>
            </div>
          </div>
        </div>
      </div>
      <div class="network flex flex-col items-center">
        <h2 class="text-5xl max-w-lg text-center mb-9">
          Huge Global Network of Fast VPN
        </h2>
        <p class="max-w-xl text-medium text-center">
          See LaslesVPN everywhere to make it easier for you when you move
          locations.
        </p>
        <div class="network__map">
          <img src="../img/map.png" alt="Map" class="cursor-pointer" />
        </div>

        <div class="network__social flex items-center gap-x-8">
          <div>
            <img src="../img/netflix.png" alt="Netflix" />
          </div>
          <div>
            <img src="../img/reddit.png" alt="Reddit" />
          </div>
          <div>
            <img src="../img/amazon.png" alt="Amazon" />
          </div>
          <div>
            <img src="../img/discord.png" alt="Discord" />
          </div>
          <div>
            <img src="../img/spotify.png" alt="Spotify" />
          </div>
        </div>
      </div>
      <customer />
    </div>
  </section>
</template>
<script>
import Customer from "./customer.vue";

export default {
  name: "features",
  components: {
    Customer,
  },
};
</script>

<style scoped>
.features {
  margin-top: 97px;
}
.features__inf-sec p,
ul {
  color: #4f5665;
}
.features__list {
  margin-left: 40px;
}
.features__list li {
  position: relative;
  margin-bottom: 12px;
}
.features__list li::before {
  content: "";
  width: 20px;
  height: 20px;
  left: -40px;
  background-size: cover;
  position: absolute;
  background: url("../img/features-list.png") no-repeat center;
}
.plan {
  padding: 13px 0;
  margin-top: 110px;
  height: 30vh;
}
.plan::before {
  width: 100%;
  height: auto;
  left: 0;
  position: absolute;
  z-index: -100;
  background-color: #e5e5e5;
  content: "";
}
.plan__items {
  width: 100%;
}
.plan__item {
  padding-top: 60px;
  width: 340px;
  height: 730px;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  background-color: #fff;
  border: 2px solid #dddddd;
}

.plan__item:hover {
  transition: 0.6s;
  border: 2px solid #f53838;
}
.plan__item img,
.plan__item .my__select {
  margin: auto;
}
.plan__item h2 {
  margin: 15px 0;
  text-align: center;
}
.plan__items .my__select {
  width: 177.88px;
}
.plan__select .btn {
  width: 177px;
}

.plan__inf {
  padding-top: 50px;
}

p {
  color: #4f5665;
}
.plan__list {
  margin-bottom: 12px;
}

.plan__list li {
  margin-bottom: 12px;
}
.plan__list li::before {
  content: "";
  display: inline-block;
  width: 24px;
  height: 24px;
  background-size: cover;
  transform: translate(-20px, 6px);
  background: url("../img/features-mark.png") no-repeat center;
}
.network {
  margin-top: 100px;
}
.network__map {
  margin-top: 140px;
}
.network__social img {
  cursor: pointer;
}
.network__social img:hover {
  filter: brightness(50%);
  transition: 0.7s;
}
@media screen and (max-width: 1000px) {
  .plan__items {
    flex-wrap: wrap;
    gap: 40px;
    justify-content: center;
  }
  .features__inf {
    align-items: center;
  }
}
@media screen and (max-width: 700px) {
  .features__inf {
    flex-wrap: wrap;
    justify-content: center;
  }
}
@media screen and (max-width: 279px) {
  .plan__item {
    border: none;
  }
}
</style>
