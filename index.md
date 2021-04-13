<style type="text/css" media="screen">
  h1 { 
    display: none; 
  }
</style>

<script>
  // This code is intended to redirect to another page immediately on load
  // but first we send an analytics event since we can't track on github.com

  !function(){var analytics=window.analytics=window.analytics||[];if(!analytics.initialize)if(analytics.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{analytics.invoked=!0;analytics.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware"];analytics.factory=function(e){return function(){var t=Array.prototype.slice.call(arguments);t.unshift(e);analytics.push(t);return analytics}};for(var e=0;e<analytics.methods.length;e++){var key=analytics.methods[e];analytics[key]=analytics.factory(key)}analytics.load=function(key,e){var t=document.createElement("script");t.type="text/javascript";t.async=!0;t.src="https://cdn.segment.com/analytics.js/v1/" + key + "/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(t,n);analytics._loadOptions=e};analytics._writeKey="eNEWxt272tQkpQEY2E2ofpRDbCCOtmBx";analytics.SNIPPET_VERSION="4.13.2";
  analytics.load("eNEWxt272tQkpQEY2E2ofpRDbCCOtmBx");
  analytics.page();
  }}();

  function redirect() {
    window.location = "https://github.com/ActivitySchema/ActivitySchema";
  }

  // some browsers block analytics.js from loading entirely, so we set a timer to 
  // check and redirect anyway if that happens
  var timeout = setTimeout(function() {
    redirect();
  }, 2000);

  analytics.ready(function() {
    clearTimeout(timeout);
    
    // Segment is ready, but it hasn't yet sent the page() call to its servers.
    // Force a dispatch call now to send, and redirect on both success and failure
    analytics.dispatch().then(redirect, redirect);
  });
</script>

loading...

