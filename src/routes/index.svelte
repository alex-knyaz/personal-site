<script>
  import Layout from './_layout_exp.svelte'
  import Octocat from '../components/svg/octocat.svelte'
</script>

<style>
  .intro {
    display: flex;
    justify-content: center;
    text-align: end;
  }

  .intro > * {
    border-radius: 10px;
    width: 256px;
    height: 246px;
  }

  .icon {
    width: 16px;
    fill: var(--fg-color);
  }

</style> 

<svelte:head>
  <title>Alex's site.</title>
</svelte:head>

<Layout>
  <span slot="title">Alex's site.</span>
  <span slot="subtitle">It's interesting, I promise!</span>
  
  <!-- BUG #3246 slot="default" -->
  <div class="intro" slot="default">
    <div>
      <p>Hi. My name is Alex.<br>
      I'm student and developer.<br>
      Contact me:</p>
      <p>📧 <a href="mailto:knyazev.al.st@gmail.com">knyazev.al.st@gmail.com</a></p>
      <p><Octocat /> <a href="https://github.com/alex-knyaz">GitHub</a></p>
    </div>
    <img src="/img/my_photo.jpg" alt="Young man with black hair"> 
  </div>

  <h2>Blog</h2>

  <ul>
    <li>Nothing here yet.</li>
  </ul>

  <h2>Projects</h2>

  <ul>
    <li> <a href="/">Personal site</a> </li>
    <li> <a href="TODO">CSS theme</a> </li>
  </ul>
</Layout>