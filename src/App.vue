<style>
@import "../src/css/main.css";
</style>

<template>
  <div class="wrapper">
    <div class="modal-container">
      <div class="image-container">
        <img class="loginImg" src="../src/img/loginFormImg.png" alt="이미지" />
      </div>
      <div class="divider"></div>
      <div class="login-form">
        <p class="loginStatus" v-if="!showNameInput">
          {{
            loggedInUser
              ? `${loggedInUser.name}님, 반갑습니다`
              : "로그인을 해주세요"
          }}
        </p>
        <p class="loginStatus" v-if="showNameInput">계정을 생성해주세요</p>
        <form>
          <div class="inputContainer">
            <input
              class="inputBox"
              type="email"
              placeholder="Email"
              v-model="email"
            />
            <input
              class="inputBox"
              type="password"
              placeholder="Password"
              v-model="password"
            />
            <input
              v-if="showNameInput"
              class="inputBox"
              type="text"
              placeholder="Name"
              v-model="name"
            />
          </div>
          <div class="buttonContainer">
            <button
              v-if="!showNameInput"
              class="button"
              type="button"
              @click="login(email, password)"
            >
              Login
            </button>
            <button v-if="!showNameInput" class="button" @click="logout">
              Logout
            </button>
            <button
              v-if="!showNameInput"
              class="button"
              @click="toggleNameInput"
            >
              SignUp
            </button>
            <button v-if="showNameInput" class="button" @click="register">
              Done
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { account, ID } from "./lib/appwrite.js";

const loggedInUser = ref(null);
const email = ref("");
const password = ref("");
const name = ref("");
const showNameInput = ref(false);

const toggleNameInput = () => {
  email.value = "";
  password.value = "";
  name.value = "";
  showNameInput.value = !showNameInput.value;
};

const login = async (email, password) => {
  await account.createEmailSession(email, password);
  loggedInUser.value = await account.get();
};

const register = async () => {
  await account.create(ID.unique(), email.value, password.value, name.value);
  login(email.value, password.value);
};

const logout = async () => {
  await account.deleteSession("current");
  loggedInUser.value = null;
};
</script>
