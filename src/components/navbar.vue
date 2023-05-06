<template>
  <div class="nav">
    <div class="logo">
      <span>WHO Academy </span>
    </div>
    
  </div>
</template>
<script setup>
const getCurrentUser = async () => {
  const response = await fetch("http://localhost:3005/api/user", {
    method: "GET",
    headers: {
      "Content-Type": "application/json",
    },
    cookie:
      "jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NiwiaWF0IjoxNjYzMTU5MjkxLCJleHAiOjE2NjMyNDU2OTF9.NdvORxlq7z2HLXePYqCDluugQN-pO8pKEYOJtZ8iGQY; ",
  });
  const res = await response.json();
  console.log(res);
  return res;
};
</script>
<style scoped>
.nav {
  z-index: 1;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  height: 80px;
  background-color: #eee;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
}

.logo {
  display: grid;
  place-items: center;
  border-bottom: 1px solid #ccc;
  border-right: 1px solid #ccc;
}

img {
  height: 30px;
  width: 30px;
}

.navelements {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  place-items: center;
}

a {
  display: grid;
  place-items: center;
  height: 100%;
  width: 100%;
  border-bottom: 1px solid #ccc;
  border-right: 1px solid #ccc;
  text-decoration: none;
  color: inherit;
}

a > span {
  display: flex;
  flex-direction: row;
  gap: 15px;
}

a > span > svg {
  transform: translateY(-8%);
}

select {
  border: none;
  background: none;
}

.flex svg {
  transform: translateY(20%);
}

.user {
  border-left: 1px solid #ccc;
}
</style>
