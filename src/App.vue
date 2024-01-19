<template>
  <main>
    <div class="card">
      <div class="topSide">
        <div class="profile">
          <img src="@/img/avatar-jessica.jpeg" alt="profile" />
        </div>
        <div class="infoSide">
          <div class="name">Jessica Randall</div>
          <div class="country">London, United Kingdom</div>
        </div>
      </div>
      <div class="midSide">
        <p>'Front-end developer and avid reader.'</p>
      </div>
      <div class="bottomSide">
        <Button
          v-for="(name, index) in buttonNames"
          :key="index"
          :name="name"
        />
      </div>
    </div>
  </main>
</template>

<script setup>
import Button from '@/components/Button.vue';

const buttonNames = ['GitHub', 'Frontend Mentor', 'LinkedIn', 'Instagram'];
</script>

<style>
:root {
  --White: hsl(0, 0%, 100%);
  --Grey: hsl(0, 0%, 20%);
  --DarkGrey: hsl(0, 0%, 12%);
  --OffBlack: hsl(0, 0%, 8%);
  --Green: hsl(75, 94%, 57%);
}

main {
  height: 100vh;
  background-color: var(--OffBlack);
  display: flex;
  justify-content: center;
  align-items: center;
}

.card {
  width: 400px;
  background-color: var(--DarkGrey);
  padding: 40px;
  border-radius: 15px;
}

.profile {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.profile img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 20px;
}

.infoSide {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.infoSide .name {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: var(--White);
}

.infoSide .country {
  font-size: 1rem;
  color: var(--Green);
  margin-bottom: 20px;
  margin-top: -5px;
}

.midSide {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px 0;
  text-align: center;
}

.midSide p {
  color: var(--White);
}
</style>
