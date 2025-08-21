<script>
  let message = 'Loading...';

  async function fetchMessage() {
    try {
      const res = await fetch('https://hanna03re.pythonanywhere.com/api/hello');
      const data = await res.json();
      message = data.message;
    } catch (err) {
      message = 'Failed to fetch message';
    }
  }

  fetchMessage();
</script>

<h1>Flask Backend Message</h1>
<p>{message}</p>
