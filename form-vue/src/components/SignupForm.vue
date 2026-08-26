<template>
  <div>
    <form>
      <label>Email:</label>
      <input type="email" required v-model="email">

      <label>password:</label>
      <input type="password" required v-model="password">

      <label for="role">Role:</label>
      <select id="role" v-model="role">
        <option value="developer">web developer</option>
        <option value="designer">web designer</option>
      </select>

      <div>
        <input type="checkbox" v-model="terms" required>
        <label>Accept terms and conditions</label>
      </div>

    </form>

    <p>Email: {{ email }}</p>
    <p>Password: {{ password }}</p>
    <p>Role: {{ role }}</p>
    <p>Terms Accepted: {{ terms }}</p>
   
  </div>
</template>

<script>

export default {
    data() {
        return {
            email: 'x@gmail.com',
            password: '',
            role: 'developer',
            terms: false,
          
        }
    }  
}
</script>

<style>
form {
    max-width: 420px;
    margin: 30px auto;
    background: #a699a690;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label  {
    color: #800068b3;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input, select {
    display: block;
    width: 100%;
    padding: 10px 6px;
    border-radius: 5px;
    border: 1px solid #a54d98aa;
    font-size: 1em;
    box-sizing: border-box;
    color: #bf5d8cd0;
}
input[type="checkbox"] {
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
}
p {
    color: rgb(152, 30, 105);
}

</style>