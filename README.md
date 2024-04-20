<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=NeKm_y0NB8w)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Enable Internet Information Services
- Install PHP Manager for IIS
- Install Rewrite Module
- Install VC Redist
- Install MYSQL
- Install osTicket
- Install HeidiSQL
- Cleanup

<h2>Installation Steps</h2>

<p>
<img width="347" alt="iis" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/55ef9054-3819-4a81-b655-45a19e9cdb99">
</p>
<p>
Click Start, open Control Panel -> Programs -> Turn Windows Features on and off -> Enable IIS/World Wide Web Services/Application Development Features -> Check boxes CGI/Common HTTP Features -> Internet Information Services -> Web Management Tools -> Check box IIS Management Console
</p>
<br />

<p>
<img width="390" alt="php manager" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/d8711c60-2624-43f5-ac48-cfad8669899c">

</p>
<p>
Download PHP Manager
</p>
<br />
<p><img width="386" alt="iis url rewrite module" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/a4bd18b6-c6b2-47fd-a283-b02a62e2d676">


</p>
<p>
Download Rewrite Module for osTicket
</p>
<br />
<p>


<img width="584" alt="cphp" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/620daef6-bb3c-45e3-9bd5-8cd19c90c56b"><img width="585" alt="php folder" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/57e8cbc8-ea16-44ab-be1f-9a5eda155ef8">


</p>
<p>
Create C:\PHP folder on C-drive -> Download PHP 7.3.8 -> Extract files into C:\PHP folder
  <p>


<img width="362" alt="vc redist" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/92a872fc-6599-476a-aa75-034a5675861c">
</p>
<p>
Download VC Redist
</p>
<br />
 <p><img width="390" alt="mysql" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/fa43d4b0-fba1-4642-8d58-42a9a9626f58">
</p>
<p>
Download MYSQL
</p>
<br />
<p>


<img width="709" alt="php admin open" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/46c7761c-9e9e-47fb-af90-4dcb20adb42c"><img width="379" alt="php path cgi" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/d736a6db-21ff-4941-981d-33b6d2be8a9c">


</p>
<p>Open IIS as administrator -> Click on PHP Manager -> Register new PHP Version -> PHP CGI -> Restart server
</p>
<br />

<p>
<img width="919" alt="move upload folder" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/128a7642-34c2-4dbe-a7df-65c232dc17cf"><img width="535" alt="change upload folder to osticket" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/75c9c9e6-07c4-4616-a589-61d92ddfe3cb">


</p>
<p>
Download osTicket -> Open c-drive/inetpub/wwwroot -> Move upload folder from osTicket download to wwwroot -> rename "upload" to "osTicket"
</p>
<br />

<p>
<img width="708" alt="browse 80" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/96279f74-25a0-4b52-b32d-1efa5d99e5ac"><img width="706" alt="enable and disable" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/f8b6527a-6670-4218-bb57-22f7e8c5e02b"><img width="377" alt="enable screen" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/849648a9-4f67-4022-acdf-7e5c78579566">



</p>
<p>
Open IIS -> Click osTicket -> Click Browse 80 -> Open PHP Manager -> Click enable or disable an extension -> Enable: php_imap.dll Enable: php_intl.dll Enable: php_opcache.dll -> Refresh osTicket

</p>
<br />

<p>
<img width="409" alt="osconfig" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/fb13bc47-16c5-4a3b-a690-b4884c563f24"><img width="575" alt="disable inheritance" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/eb0e64a7-38c3-4e8e-a7d9-c234c512a817"><img width="345" alt="new perms everyone" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/ea44d9c9-2b18-4587-90c4-1c0852695252">



</p>
<p>
Change From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php -> basically just delete sample from file name -> Disable inheritance -> Set a principal -> Set permission to Everyone -> Check all boxes
</p>
<br />

<p>
<img width="480" alt="server setup" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/36f11a12-6e75-4947-8abc-25900182be76"><img width="449" alt="heidisql" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/e1f2d1ee-f588-411e-b678-ec04952e5b2e"><img width="701" alt="setup database" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/f855dc67-9c0b-4489-9f34-3b579f4e7af5"><img width="299" alt="osticket login" src="https://github.com/qjackson14/osticket-prereqs/assets/156969011/cf80c512-471c-4812-b887-9296c4c6071a">

</p>
<p>
Open osTicket -> Download HeidiSQL -> Create new/database/osTicket -> Click install now & login

</p>
<br />
