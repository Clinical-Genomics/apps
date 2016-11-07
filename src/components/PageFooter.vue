<template>
  <footer class="footer">
    <h1>Clinical Genomics</h1>
    <div class="logo">
      <img src="../assets/clinical-logo.png">
    </div>
  </footer>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style>
  .footer {
    display: flex;
    align-items: center;
    justify-content: flex-end;

    padding: 1rem;
    background-color: rgba(239, 124, 0, .3);
  }

  .logo {
    width: 50px;
    height: 50px;
  }

  img {
    max-width: 100%;
  }

  h1 {
    font-size: 1.5rem;
    color: #444;
    font-weight: 600;
    margin-right: 1rem;
  }

  /* Small Devices, Tablets */
  @media (min-width: 768px) {
    .footer {
      padding: 1rem 3rem;
    }

    .logo {
      width: 75px;
      height: 75px;
    }

    h1 {
      font-size: 2rem;
    }
  }
</style>
