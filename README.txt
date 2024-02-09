Extending control

	- Need to install the Controls package if wanting to extend from an existing control
	- In Descirption.json need to change base to correct control
	"base": "TcHmi.Controls.Beckhoff.TcHmiButton"

	- In Template.html, need the controls base html
	    <div class="TcHmi_Controls_Beckhoff_TcHmiButton-template tchmi-button-template tchmi-box">
	        <span class="TcHmi_Controls_Beckhoff_TcHmiButton-template-content-text tchmi-button-template-content-text"></span>
	    </div>
	
	- Manifest.json needs the Controls package added
		    {
		      "type": "Package",
		      "nugetId": "Beckhoff.TwinCAT.HMI.Controls"
		    },
	
	- Tsconfig.tpl.json needs to include the controls ts file
	
	    "$(Beckhoff.TwinCAT.HMI.Controls).InstallPath/TcHmiButton/TcHmiButton.d.ts"
	
	- The .ts file needs to have the class extended for the control
	export class <FrameworkControl Class> extends TcHmi.Controls.Beckhoff.TcHmiButton
	
