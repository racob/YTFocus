<script>
	import browser from "webextension-polyfill";

	let queryInfo = { active: true, currentWindow: true }
	var activeURL = ""

	chrome.tabs.query(queryInfo, getURLFromActiveTab)

	function getURLFromActiveTab(tabs) {
		let activeTab = tabs[0]
		console.log(activeTab.url);
		activeURL = activeTab.url
	}

</script>
  
<main>
	<p>{activeURL}</p>
</main>