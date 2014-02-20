---
layout: blog
title: Step-by-step: creating and installing a package for Commotion
categories: chat,applications,routers,,messaging
created: 2012-10-08
changed: 2012-11-21
post_author: The Work Department
lang: en
---
  <p>Here at The Work Department, we&#39;ve been busy cooking up systems to experiment with applications that utilize node-to-node mesh connections and are eager to share them with you. In particular, some of the example applications that we proposed in our <a class="external" href="https://commotionwireless.net/blog/exploring-meshaging" target="_blank">Exploring &quot;Meshaging&quot;</a> post have been taking form. We want to offer you the tools to experiment with what is possible given the unique architecture of a mesh network.</p>
<p>The Commotion router software is built atop OpenWRT, a Linux distribution designed for routers and other small devices. OpenWRT has a package management system, and Commotion&rsquo;s code is kept in a separate feed and package. A developer can integrate additional features into a Commotion network by writing or porting applications and packaging them for OpenWRT. Below, we explain the process of porting and packaging an application (in this case, a small websockets server, ws-routing, and dependencies).</p>
<pre linenumbers="off">
# Clone the commotion-openwrt repo: 
git clone https://github.com/opentechinstitute/commotion-openwrt.git 
cd commotion-openwrt 
./setup.sh 
cd ..
 # Clone your package repo: 
git clone https://github.com/bnchdrff/commotion-wsrouting-feed.git commotion-examples
 # Run the package setup.sh script: 
cd commotion-examples 
./setup.sh # ignore package feed errors
 # Configure and build: 
cd ../commotion-openwrt/openwrt
 make menuconfig # ignore package feed errors
 # A ncurses GUI will display: 
## Select the commotion-apps submenu
 ## Select ws-routing as * (static) by pressing Y 
## Select exit 
## When prompted, choose to save config 
make V=99 # build, verbosely 
cd bin/ar71xx/
 ls</pre>
<p>And, voilà! You should see a list of files that look something like this: &quot;<strong>openwrt-ar71xx-generic-ubnt-bullet-m-squashfs-factory.bin</strong>&quot;. The file you&#39;ll need to flash your wireless router will vary depending on the router hardware. Using that file, follow the instructions provided for <a class="external" href="https://code.commotionwireless.net/projects/commotion-manual/wiki/Installing_Commotion_on_Wireless_Nodes" target="_blank">Installing Commotion on Wireless Nodes</a> in order flash the router. These <a class="external" href="https://code.commotionwireless.net/projects/commotion-manual/wiki/Detailed_TFTP_Instructions" target="_blank">Detailed TFTP Instructions</a> also include detailed steps to transfer the file to your router with <strong>TFTP.</strong></p>
<h3>Get a taste of Commotion</h3><p>Well done! You have installed Commotion on a your wireless router. After the router restarts, you can disable your wired network and hop on the &ldquo;commotion_NNNNN_ap&rdquo; network that should become available. Open a web browser and navigate to any website, which should bring you to the Commotion splash page. Last, you can verify that the <strong>ws-routing</strong> package is installed by following these steps:</p>