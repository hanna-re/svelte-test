<script>
  let message = "Loading...";

  async function fetchMessage() {
    const res = await fetch("https://yourusername.pythonanywhere.com/api/hello");
    const data = await res.json();
    message = data.message;
  }

  fetchMessage();
</script>

<h1>Flask + SvelteKit</h1>
<p>{message}</p>
