Online Advertising SYSTEM


ABSTRACT

Online advertising is a major economic force in the Internet today, funding a wide variety of websites and services. Today’s deployments, however, erode privacy and degrade performance as browsers wait for ad networks to deliver ads. This paper presents Privad, an online advertising
system designed to be faster and more private than existing systems while filling the practical market needs of targeted advertising: ads shown in web pages; targeting based on keywords, demographics, and interests; ranking based on auctions; view and click accounting; and defense against click-fraud. Privad occupies a point in the design space that strikes a balance between
privacy and practical considerations. This paper presents the design of Privad, and analyzes the pros and cons of various design decisions. It provides an informal analysis of the privacy properties of Privad. Based on microbenchmarks and traces from a production advertising platform, it shows that Privad scales to present-day needs while simultaneously improving users’ browsing experience and lowering infrastructure costs for the ad network. Finally, it reports on our implementation of Privad and deployment of over two thousand clients.


EXISTING SYSTEM


The existing system has many shortcomings associated with it. In the existing system there is  no maintaining of secret key (encryption and decryption) inorder to download add. So untrusted broker and untrusted dealer would easily hack add which is uploaded by advertiser or   publisher.So there is no privacy for the advertiser. It provides an informal analysis of the privacy properties of Privad. There is no privacy in existing while uploading the add.


PROPOSED SYSTEM

This paper presents Privad, an online advertising system designed to be faster and more private than existing systems while filling the practical  market  needs of targeted advertising: ads shown in web pages; targeting based on keywords, demographics, and interests; based on auctions; view and click accounting; and defense against click-fraud. Privad include commercial viability. This section provides details on ad dissemination, ad auctions, view/click reporting and click-fraud defense. It also puts forth some of the rationale for our design decisions. These details represent a snapshot of our current thinking. While ad dissemination, reporting are quite stable, the click-fraud defense, and auctions may easily evolve as we do more analysis and testing. We present them here so as to present a complete argument for Privad’s viability.

THE PRIVAD ARCHITECTURE







MODULE DESCRIPTION


Number of Modules
After careful analysis the system has been identified to have the following modules:

Ad Dissemination Module
Ad Auctions Module
View/Click Reporting Module
Click Fraud Defense Module

Ad Dissemination Module

The most privacy-preserving way to disseminate ads would be for the broker to transmit all ads to all clients.The pub-sub protocol consists of a client’s request to join a channel   followed by the broker serving a stream of ads to the client. Channels are defined by the broker. The complete set of channels is known to all clients, for instance by having dealers host a copy (signed by the broker). A client joins a channel when its profile attributes match those of the channel. The join request transmitted to the broker. The broker attaches with ads published, which the dealer uses to lookup the intended client to forward the ads to. The broker determines which ads should be sent and for how long they should be cached at the client. For instance, the broker stops sending ads for an advertiser when the advertiser nears his budget limit. Note that not all ads transmitted are appropriate for the user, and so may not be displayed to the user. Over time, the broker can estimate the number of ads that must be sent out for a particular advertiser 
to generate a target number of views and clicks.


                                    


2. Ad Auctions Module

Auctions determine which ads are shown to the user and in what order. The broker can estimate the number of ads that must be sent out for a particular advertiser to generate a target number of views and clicks. A simple auction from this design space goes as follows. The broker periodically runs the auction over the set of ads targeted to a given pub-sub interest channel, producing a ranked set of ads.




3.View/ClickReportingModule
        
Ad views and clicks, as well as other ad-initiated user activity need to be reported to the broker. The protocol for reporting ad events  is straightforward. The report containing the addname, publisher name, and type of event (view, click, etc.) and sent through to the advertiser. The advertiser view the user clicks which it uses later to trace suspected click-fraud reports in a privacypreservingmanner.



4. Click Fraud Defense Module

Click-fraud consists of users or on ads for the purpose of attacking one or more parts of the system. Generally speaking, privacy makes click-fraud more challenging because clients are hidden from the broker. Privad addresses this challenge through an explicit privacy-preserving protocol between broker and dealer. Both the broker and dealer participate in detecting and blocking click-fraud; the broker by looking at overall click behavior for advertisers Blocking a fraudulent client once an attack is detected is straightforward. When a publisher or advertiser is under attack , the broker tells the advertiser which report username are suspected as being involved in click-fraud. The broker traces the username back to the client, and if the client is implicated more than some set threshold, subsequent reports from that client are blocked.

Software requirements: 


          Operating System		: Windows
          Technology			: Java and J2EE
          Web Technologies		: Html, JavaScript, CSS
           IDE				            : My Eclipse
           Web Server			: Tomcat
           Database			: My SQL
           Java Version		            : J2SDK1.5                  

Hardware requirements:

         Hardware                             -     Pentium 
         Speed                                   -     1.1 GHz
         RAM                                   -    1GB
         Hard Disk                           -    20 GB
         Floppy Drive                       -    1.44 MB
         Key Board                          -    Standard Windows Keyboard
         Mouse                                 -    Two or Three Button Mouse
         Monitor                               -    SVGA

