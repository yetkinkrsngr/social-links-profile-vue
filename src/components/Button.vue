<template>
  <div>
    <button>{{ name }}</button>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
  },
};
</script>

<style>
button {
  width: 100%;
  padding: 14px;
  margin-top: 15px;
  background-color: var(--Grey);
  border: none;
  color: var(--White);
  font-weight: 600;
  border-radius: 10px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
button:hover {
  background-color: var(--Green);
  color: var(--OffBlack);
}
button:active {
  background-color: var(--DarkGrey);
}
</style>
