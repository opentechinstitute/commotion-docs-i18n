---
layout: blog
title: Building Pop-up Mesh Networks
tags: [pop-up mesh, urban]
created: 2013-10-30
changed: 2013-12-19
post_author: Ryan Gerety
lang: en
---
  <img alt="" class="media-image attr__typeof__foaf:Image img__fid__548 img__view_mode__media_large attr__format__media_large" height="222" src="/files/styles/large/public/title_image.png?itok=uhJC0pqH" typeof="foaf:Image" width="480" />
The Open Technology Institute recently conducted a training on how to build pop-up mesh networks using Commotion. Our goal was to quickly deploy a flexible and mobile mesh network across several square blocks using portable battery-powered routers carried in backpacks. <!--more-->Commotion’s dynamic routing allows a network to shift and transform with the movements of the people, creating a highly resilient temporary infrastructure that can distribute Internet access throughout an area or support local area communications and data sharing.
In this blogpost, we describe three field trials conducted by participants during the training. In the field trials we used Ubiquiti omnidirectional PicoStation M2 routers and Energizer XP8000 battery packs. These battery packs are compact and able to provide 3-4 hours of power to the routers, but any battery pack that meets the power requirements of the router would suffice - for example, the PicoStations can run on voltages from 15 to 24 volts. The battery packs supply 20 volts. Refer to the voltage markings on your router's power supply before choosing a battery.
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__561 img__view_mode__media_large attr__format__media_large" height="161" src="/files/styles/large/public/equipment_0.png?itok=HPlApBYr" typeof="foaf:Image" width="480" />
At the beginning of the training, participants learned how to install and configure Commotion, mesh several routers together and assess link quality. With these skills, participants went outside and tested the potential reach of the signal at street level of two routers powered by portable battery packs.
Ubiquiti estimates that PicoStations can cover up to 500 meters, but every environment has different properties that impact wireless propagation. As with permanent rooftop wireless networks, pop-up networks are impacted by buildings, vegetation, line of sight and other wireless barriers. Street level networks are also impacted by traffic, parked cars, crowds of people and small hills.
In these distance tests, participants found that link quality degraded after approximately 200 meters and broke at approximately 300 meters apart. This estimate proved consistent with our <a href="http://oti.newamerica.net/blogposts/2013/commotion_field_test_pop_up_mesh_network_downtown_washington_dc-93217"> previous fields test</a> near the Open Technology Institute's offices, although we were in a different location. Participants monitored link quality with their smartphones using the Commotion interface to see ETX values and signal strength and Fing to measure ping times.
<table border="0" cellpadding="0" cellspacing="0" style="width: 427px;" width="427px">
	<tbody>
		<tr>
			<td width="300px"><img alt="" class="media-image attr__typeof__foaf:Image img__fid__549 img__view_mode__media_large attr__format__media_large" src="/files/styles/large/public/p2p.png?itok=SZDHeK_0" style="width: 300px; height: 211px;" typeof="foaf:Image" /></td>
			<td width="127px"><img alt="" class="media-image attr__typeof__foaf:Image img__fid__559 img__view_mode__media_large attr__format__media_large" src="/files/styles/large/public/Screenshot_2013-10-29-13-30-11_0.png?itok=E5zClkvu" style="width: 127px; height: 211px;" typeof="foaf:Image" /></td>
		</tr>
	</tbody>
</table>
<i>Map 1: Two node distance test.</i>
We repeated the distance tests and link monitoring exercises, which helped participants develop an intuitive sense of network planning and management. We developed these skills further with our interactive network design and engineering activities, “Wireless Challenges” and “<a href="https://commotionwireless.net/docs/cck/planning/design-your-network-every-network-tells-story">Every Network Tells A Story</a>,” before moving on to more complex network configurations.
Participants then created a network and connected it to the Internet through a gateway Commotion node in a window attached to an ADSL Internet connection. Participants tested this new connection across a more diverse streetscape, adding more nodes to the network. With an Internet gateway on the mesh, participants and OTI staff were able to make VOIP calls and check email while spread out along the street corners.
Participants spread out along the streets until each network connection became weak, inhibiting those online activities. Participants found that traffic and parked cars negatively impacted the maximum link distance and used the skills from the earlier activities to solve those problems. The network is shown in Map 2.
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__551 img__view_mode__media_large attr__format__media_large" height="294" src="/files/styles/large/public/map2.png?itok=n-xrL_wd" typeof="foaf:Image" width="389" />
<i>Map 2: 6 node field trial with Internet gateway.</i>
In the third field trial, participants deployed a network to cover a larger street in a more crowded area and extend the network into smaller side streets. Participants stationed individuals and their portable mesh nodes at particular corners, establishing a stationary backbone of the network. Other participants were roaming nodes; they walked along the back streets to establish network coverage along those streets and experiment with dynamically changing the network. The general configuration is shown in Map 3, as are network statistics captured during the field trial.
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__552 img__view_mode__media_large attr__format__media_large" height="319" src="/files/styles/large/public/map3.png?itok=Z-XI2qdf" typeof="foaf:Image" width="390" /> 
<i>Map 3: 8 node field trial with 7 people remaining relatively stationary and two people moving throughout the area.</i>
In this configuration, node 50 moved throughout the network while other nodes remained relatively stationary. Nodes 37 and 182 occasionally had difficulty maintaining connections to the rest of the network. This was both because it was difficult to stand within line of sight, and because those participants had less field experience adjusting their position to improve network performance.
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__553 img__view_mode__media_large attr__format__media_large" height="276" src="/files/styles/large/public/olsrviz4.png?itok=hYCCbEeN" typeof="foaf:Image" width="475" />
<i>Image 1: Network visualized with ETX values at point \[4\] (the last digits of the IP address correspond to the numbers in the map).</i>
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__554 img__view_mode__media_large attr__format__media_large" height="240" src="/files/styles/large/public/olsrviz6.png?itok=RtTLCP_Y" typeof="foaf:Image" width="480" />
<i>Image 2: Network visualized with ETX values at point \[6\] (the last digits of the IP address correspond to the numbers in the map). </i>
<img alt="" class="media-image attr__typeof__foaf:Image img__fid__555 img__view_mode__media_large attr__format__media_large" height="216" src="/files/styles/large/public/olsrviz7.png?itok=oxbB0fsK" typeof="foaf:Image" width="480" />
<i>Image 3: Network visualized with ETX values at point \[7\] (the last digits of the IP address correspond to the numbers in the map).</i>
In this field trial, we did not have an available Internet gateway, but instead, used <a href="https://github.com/danstaples/MediaGrid">MediaGrid</a> to facilitate local secure communications across the mesh network. During this exercise, we had MediaGrid running on a single laptop in the network. However, MediaGrid has the ability to sync across multiple laptops, which increases the resilience of the network. MediaGrid has a chat feature that allowed the deployment team to discuss changes to the network node position and report link quality and signal strength over the local area network.
<table border="0" cellpadding="0" cellspacing="0" style="width: 338px;" width="338px">
	<tbody>
		<tr>
			<td width="169px"><i><img alt="" class="media-image attr__typeof__foaf:Image img__fid__556 img__view_mode__media_large attr__format__media_large" src="/files/styles/large/public/mediagrid1.png?itok=XYdP47ke" style="width: 169px; height: 300px;" typeof="foaf:Image" /></i></td>
			<td width="169px"><i><img alt="" class="media-image attr__typeof__foaf:Image img__fid__558 img__view_mode__media_large attr__format__media_large" src="/files/styles/large/public/mediagrid2_0.png?itok=-5kIuikp" style="width: 169px; height: 300px;" typeof="foaf:Image" /></i></td>
		</tr>
	</tbody>
</table>
<i>Image 4: Screenshots of the MediaGrid mobile web interface.</i>
While we ran a local application on the network for these experiments, the network could also be connected to a 3G modem, an Internet gateway inside of a building, or a long distance link to another part of the city.
The field experiments resulted in the following conclusions:
<ul>
	<li>Because the network can be highly dynamic, people must adequately plan and constantly coordinate to both maintain solid network links and provide adequate coverage by remaining spaced apart. This is easier when some nodes are relatively stationary.</li>
	<li>The network was most resilient when there were multiple redundant links. Although links could stretch several blocks, it was often ideal to place nodes on opposite sides of the street but only one block apart and create redundancy in the network.</li>
	<li>Adding height to the ground-level nodes improved performance by reducing the number of wireless barriers (for example, people standing between the nodes). Going up half a flight of stairs improved network quality between those links.</li>
	<li>Coordinating across a large geography is difficult, making pre-planning important. Especially for purposes of field experiments, everyone should have all positions mapped, everyone’s IP address and a method of communication.</li>
</ul>
The Commotion project is currently working on the <a href="https://commotionwireless.net/docs/cck">Commotion Construction Kit,</a> a set of tools that the Open Technology Institute has used in trainings around the world and at home. It is a “do it ourselves” guide to building wireless mesh networks. They are a work in progress, so check back frequently for updates. We welcome feedback and experimentation!
These field experiments were conducted using <a href="https://commotionwireless.net/download/routers">Commotion Developer Release 2</a>, and the network was configured to use WPA2-PSK to encrypt the traffic.
 