<html>
   <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DRR00000DbT9F',
				'MIAW_Service_Deployment_Web_Chat',
				'https://pplprs--deveray.sandbox.my.site.com/ESWMIAWServiceDeploymen1740792445980',
				{
					scrt2URL: 'https://pplprs--deveray.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
   </script>
   <script type='text/javascript' src='<Please use the JS URL from your Snippet Code >' onload='initEmbeddedMessaging()'></script>
   <div style="position: fixed; bottom: 35px; right: 35px; border-radius: 40px; background: #801818; cursor: pointer; color: white">
         <div onclick="launchChat()">
            <img 
               src="<Please use your image>"
               style="border-radius: 50%; float:left; margin: 5px;"
               height="50px"
               width="50px"/>
	       <h3 style="float:right;">Hi, How can I help you?</h3>
         </div>
   </div>
   <script>
	function launchChat() {
           embeddedservice_bootstrap.utilAPI.launchChat()
               .then(() => {
                   console.log(
                       'Successfully launched Messaging'
                   );
               }).catch(() => {
                   console.log(
                       'Some error occurred when launching Messaging'
                   );
               }).finally(() => {
                   console.log(
                       'Successfully launched Messaging - Finally'
                   );
               });
       }
   </script>
</html>
