<script>
	import InnerDispatch from './InnerDispatch.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}

  function handleMyNickName(event) {
    alert(event.detail.axel)
  }

	function handleSayDosen(e) {
		alert(e.detail.message)
	}
</script>

<InnerDispatch on:myDosenName={handleSayDosen}/>
