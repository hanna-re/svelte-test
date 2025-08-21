<script>
  let message = "Loading...";

  async function fetchMessage() {
    try {
      const res = await fetch("https://yourusername.pythonanywhere.com/api/hello");
      const data = await res.json();
      message = data.message;
    } catch (err) {
      message = "Error fetching message";
    }
  }

  fetchMessage();
</script>

<h1>Flask + SvelteKit</h1>
<p>{message}</p>
