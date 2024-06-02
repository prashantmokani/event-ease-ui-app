<script setup lang="ts">
import { ref } from 'vue'
function toggle(event) {
    const sidebar = document.querySelector('.sidebar');
    sidebar.classList.toggle('expanded');
}
</script>

<template>
<div class="sidebar">
    <div class="logo">
      <img src="../../assets/vue.svg" alt="Logo" @click="toggle">
    </div>
    <ul class="menu">
      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/dashboard.svg" alt="Dashboard"></span>
          <span class="title">Dashboard</span>
        </a>
      </li>
      <li>
        <a href="#">
          <span class="iconImg"><img src="../../assets/navbar/icons/members.svg" alt="Members"></span>
          <span class="title">Members</span>
        </a>
      </li>
      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/events.svg" alt="events"></span>
            <span class="title">Events</span>
        </a>
      </li>
      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/income.svg" alt="Income"></span>
          <span class="title">Income</span>
        </a>
      </li>
      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/expense.svg" alt="Expense"></span>
          <span class="title">Expense</span>
        </a>
      </li>

      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/reports.svg" alt="Reports"></span>
            <span class="title">Reports</span>
        </a>
      </li>
      <li>
        <a href="#">
            <span class="iconImg"><img src="../../assets/navbar/icons/logout.svg" alt="Logout"></span>
          <span class="title">Log Out</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<style scoped>
body {
    display: flex;
    margin: 0;
    font-family: "Roboto", sans-serif;
    font-weight: 500;
    font-style: normal;
  }
  .sidebar {
    width: 80px;
    height: 100vh;
    background: #fff;
    border-right: 1px solid #e0e0e0;
    transition: width 0.3s;
    overflow: hidden;
    position: fixed;
  }
  
  .sidebar.expanded {
    width: 250px;
  }
  
  .logo {
    padding: 20px;
    text-align: center;
  }
  
  .logo img {
    width: 40px;
  }
  
  .menu {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .menu li {
    display: flex;
    align-items: center;
  }
  
  .menu a {
    text-decoration: none;
    color: #333;
    display: flex;
    align-items: center;
    padding: 15px 20px;
    width: 100%;
    transition: background 0.3s;
  }
  
  .menu a:hover {
    background: #f0f0f0;
  }
  
  .icon {
    font-size: 24px;
    margin-right: 20px;
  }

  .iconImg {
    text-align: center;
    width: 30px;
    margin-right: 20px;
    transition: opacity 0.3s;
  }
  
  .title {
    display: none;
    transition: opacity 0.3s;
  }
  
  .sidebar.expanded .title {
    display: inline-block;
  }
  
  .content {
    margin-left: 80px;
    padding: 20px;
    transition: margin-left 0.3s;
    flex-grow: 1;
  }
  
  .sidebar.expanded ~ .content {
    margin-left: 250px;
  }
  
  .toggle-btn {
    background: #007bff;
    color: #fff;
    border: none;
    padding: 10px;
    cursor: pointer;
    border-radius: 5px;
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    transition: left 0.3s;
  }
  
  .sidebar.expanded .toggle-btn {
    left: 50%;
    transform: translateX(-50%);
  }
  
</style>
