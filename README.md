# Perform a Query With Google Chronicle
This project is meant to display competence and comfortability with Google's Chronicle, a cloud-native tool, to investigate a security incident involving phishing and answer a series of questions.

<h2>Scenario:</h2>

You are a security analyst at a financial services company. You receive an alert that an employee received a phishing email in their inbox. You review the alert and identify a suspicious domain name contained in the email's body: signin.office365x24.com. You need to determine whether any other employees have received phishing emails containing this domain and whether they have visited the domain. You will use Chronicle to investigate this domain.


<h2>Perform Domain Search</h2>
<img src="https://i.imgur.com/9AfgtBP.png" height="80%" alt="Perform Search"/> <br />

<br />
<br />

<h2>Evaluate Search Results</h2>
In this step, it is important to evaluate the nececessary sections of Chronicle in order to gain all relevent information. Pictures of several different sections will be provided below: <br />
<br />

Main Page: <br />
This page includes many different resources, including WHOIS information, Prevalence, Resolved IPs, Sibling Domains, ET Intelligence Rep List, and more. <br />
<img src="https://i.imgur.com/YydApOI.png" height="80%" alt="Evaluate Results 1"/> <br />

VT Context:<br />
This section provides VirusTotal information for the domain. <br />
<img src="https://i.imgur.com/q9AOu2i.png" height="80%" alt="Evaluate Results 2"/> <br />

<br />
<br />

<h2>Investigate Threat Intelligence Data</h2>
In this step, we go further into the investigation by accessing the domain view for 'office365x24.com', viewing the VT Context of the Top Private Domain, and take note of the category listen in the ET Intelligence Rep  List.
<br />

Move to and inspect Top Private Domain: <br />
<img src="https://i.imgur.com/VSfP1Vd.png" height="80%" alt="Investigate Intel Data 1"/> <br />
<img src="https://i.imgur.com/JLIXxke.png" height="80%" alt="Investigate Intel Data 2"/> <br />

ET Intelligence Rep List: <br />
<img src="https://i.imgur.com/SV0oqAF.png" height="80%" alt="Investigate Intel Data 3"/> <br />
Note that the category listed is "Drop site for logs or stolen credentials".

<br />
<br />

<h2>Investigate Affected Assets and Events</h2>
In this step we explore the Assets and Timeline sections, which provide information about events and interactions made with this domain and the assets that have accessed it: <br />
<img src="https://i.imgur.com/nUEYddc.png" height="50%" alt="Investigate Assets and Events 1"/> 
<img src="https://i.imgur.com/MlnshCM.png" height="60%" alt="Investigate Assets and Events 2"/> <br />

Open the raw log viewer of the first POST /login.php entry: <br />
<img src="https://i.imgur.com/9VPZeqt.png" height="80%" alt="Investigate Assets and Events 3"/> 

<br />
<br />

<h2>Investigate Resolved IP Address</h2>
In this step, we investigate the IP addresses found under the "RESOLVED IPS" insight card to identify if the signin.office365x24.com domain uses another domain. We must take note of the Timeline, Assets, and Domains sections.<br />

Timeline:<br />
In this instance, we must take note of the additional 'Post' request. A new post sugests that an asset may have been phished.<br />
<img src="https://i.imgur.com/E1Jdvrh.png" height="80%" alt="Investigate Resolved Addresses 1"/> <br />

Assets: <br />
We must take note of the additional affected assets.<br />
<img src="https://i.imgur.com/hoWaDC4.png" height="80%" alt="Investigate Resolved Addresses 2"/> <br />

Domains: <br />
We must take note of the additional domains associated with this IP address.
<img src="https://i.imgur.com/GLmyICc.png" height="80%" alt="Investigate Resolved Addresses 3"/> <br />


<br />
<br />

<h4>End of Project</h4>
