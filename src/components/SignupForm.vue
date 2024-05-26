<template>
  <form>
    <label>
      Email:
      <input type="email" required v-model="email">
    </label>
    <label>
      Password:
      <input type="password" required v-model="password">
    </label>
    <label>
      Role:
      <select name="role" v-model="role">
        <option value="developer">Developer</option>
        <option value="designer">Designer</option>
      </select>
    </label>
    <p>{{email}}</p>
    <p>{{password}}</p>
    <p>{{role}}</p>
  </form>
</template>

<script>
export default {
  data() {
    return {
      password: '',
      email: '',
      role: 'designer',
    }
  }
}
</script>

<style>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 0 0 25px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
  width: 100%;
}
input, select {
  margin-top: 5px;
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
</style>