<script>
  import { url, isActive } from "@roxi/routify";
  import Icon from 'svelte-awesome';
  import { bars } from 'svelte-awesome/icons';

  const _links = [
    ["./index", "Home"],
    ["./research", "Research"],
    ["./publications", "Publications"],
    ["./people", "People"],
    ["./software", "Software"],
    ["./join-us", "Join Us"],
  ];

  let hide = true;
  function collapseMenu() {
    hide = !hide;
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap');

  .title {
    font-family: 'Orbitron', sans-serif;
    font-size: 45px;
  }

  .navbar {
    text-align: center;
    overflow: hidden;
  }

  .navbar a {
    color: inherit;
    display: inline-flex;
    border: 1px solid transparent;
    padding: 12px 14px;
    margin: 16px 5px;
    text-decoration: none;
  }

  .navbar a:hover {
    border: 1px solid black;
  }

  .icon {
    position: relative;
    right: 5px;
    top: 3px;
  }

  .menu {
    display: none;
  }
  
  @media (max-width: 640px) {
    .title {
      display: none;
    }

    .navbar a {
      padding: 12px;
      margin: 5px;
      display: block;
      text-align: left;
    }

    .menu {
      display: inline-block;
      text-align: left;
      padding: 15px;
      cursor: pointer;
    }

    .menu .title {
      font-family: 'Orbitron', sans-serif;
      font-size: 25px;
      display: inline-flex;
    }

    .navbar .hide {
      display: none;
    }
  }

</style>

<div class="navbar">
  <div class="title">
    CheungLab
  </div>
  <div class="menu" on:click={collapseMenu}>
    <span class="icon"><Icon data="{bars}" scale=1.5/></span>
    <span class="title">CheungLab</span>
  </div>

  <div class:hide>
  {#each _links as [path, name]}
    <a class="link" class:active={$isActive(path)} href={$url(path)}>
      {name}
    </a>
  {/each}
  </div>
</div>
