<script>
	import InnerDispatch from './InnerDispatch.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}

  function handleMyNickName(event) {
    alert(event.detail.axel)
  }
</script>

<InnerDispatch on:adam={handleMyNickName}/>
