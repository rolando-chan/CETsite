<html>
  <head><meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1"></head>
  <body>
  <p><a id="editThisPageLink" target="_blank" style="color:blue">Edit this page</a></p>
<script>document.getElementById('editThisPageLink').href = "https://github.com/ESW1234/esw1234.github.io/edit/master" + window.location.pathname;</script>
    <style type='text/css'>
	.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #1BCE36;
		font-family: "Times New Roman", sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #1BCE36;
	}
	    
</style>
<!-- 
  NA44 STMFB ORG: <username> / <password>
-->
<!-- <script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script> -->
<script type='text/javascript'>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //Or false
		embedded_svc.settings.language = 'en-US'; //For example, enter 'en' or 'en-US'

		//embedded_svc.settings.defaultMinimizedText = '...'; //(Defaults to Chat with an Expert)
		//embedded_svc.settings.disabledMinimizedText = '...'; //(Defaults to Agent Offline)

		//embedded_svc.settings.loadingText = ''; //(Defaults to Loading)
		//embedded_svc.settings.storageDomain = 'yourdomain.com'; //(Sets the domain for your deployment so that visitors can navigate subdomains during a chat session)

		// Settings for Chat
		//embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
			// Dynamically changes the button ID based on what the visitor enters in the pre-chat form.
			// Returns a valid button ID.
		//};
		embedded_svc.settings.prepopulatedPrechatFields = {FirstName: "Random", LastName: "User", Email: "randomuser@salesforce.com"};//, Company: "Salesforce", Priority: "Medium", Subject: "Help me"}; //Sets the auto-population of pre-chat form fields
		//embedded_svc.settings.fallbackRouting = []; //An array of button IDs, user IDs, or userId_buttonId
		//embedded_svc.settings.offlineSupportMinimizedText = '...'; //(Defaults to Contact Us)
		
		//embedded_svc.settings.smallCompanyLogoImgURL = 'http://esw1234.github.io/smallCompanyLogoImg.png';

		embedded_svc.settings.enabledFeatures = ['LiveAgent'];
		embedded_svc.settings.entryFeature = 'LiveAgent';
		
		// Debug mode.
		embedded_svc.settings.devMode = false;

		embedded_svc.init(
			'https://snapins.my.stmfb.stm.salesforce.com',
			'https://sites.stmfb.stm.force.com',
			gslbBaseURL,
			'00DRM0000005jYI',
			'NishantMenonDeployment',
			{
				baseLiveAgentContentURL: 'https://c.la2-stmfb1-0-prd.stmfb.stm.salesforceliveagent.com/content',
				deploymentId: '572RM0000004DDM',
				buttonId: '573RM000000068s',
				baseLiveAgentURL: 'https://d.la2-stmfb1-0-prd.stmfb.stm.salesforceliveagent.com/chat',
				eswLiveAgentDevName: 'EmbeddedServiceLiveAgent_Parent04IRM0000004Dq42AE_17428a5e7ef',
				isOfflineSupportEnabled: true
			}
		);
	};
	
	if (!window.embedded_svc) {
		var s = document.createElement('script');
		s.setAttribute('src', 'https://snapins.lightning.stmfb.stm.force.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW('https://service.force.com');
	}
</script>
  </body>
</html>

