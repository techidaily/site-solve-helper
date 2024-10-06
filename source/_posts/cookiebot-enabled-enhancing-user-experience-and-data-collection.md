---
title: "Cookiebot-Enabled: Enhancing User Experience and Data Collection"
date: 2024-09-29T00:58:40.034Z
updated: 2024-10-06T05:16:33.978Z
categories:
  - abbyy
thumbnail: https://thmb.techidaily.com/696965aa1a0f4c21fdfd456761bb63f354f50ffc3b27173b44a827d0fae8995e.jpg
---

## Cookiebot-Enabled: Enhancing User Experience and Data Collection

[Back to ABBYY Blog](https://tools.techidaily.com/abbyy/products/)

# What We Learned at JSConf Budapest 2022

###### Attila Kling

October 27, 2022

![](https://static1.abbyy.com/abbyycommedia/36301/jsconf_cover.jpg) 

This summer, ABBYY was a proud sponsor of [JSConf Budapest—](https://jsconfbp.com/)an international conference bringing together JavaScript enthusiasts from all over the world. Six people from the ABBYY Hungary team, including myself, were representing the company at the event. During the two-day conference, we got to talk to hundreds of developers from as far afield as Singapore, Israel, Serbia, the UK, and many other locations. A steady stream of visitors attended our booth where everyone could take our fun (but not so easy) quiz and win prizes, while learning about ABBYY. We also had the opportunity to listen to dozens of great speakers, and collected some interesting thoughts and insights to share in this post\*.

### **The Power of JS Generators by Anjana Vakil**

In this presentation, Anjana shared her passion about generators with the audience with so much energy that even if you didn’t know anything about generators, you were instantly hyped up!

The presentation started with a brief introduction to generators. In case your generator-related knowledge is a little bit rusty, here's a [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global%5FObjects/Generator) to refresh your memory, but I advise you to watch Anjana's presentation instead, which has it all covered.

_Iterables_

Generator functions are also iterables which means we can loop through them, and we can use, for example, the spread operator:

function\* abcs() {

 yield 'a';

 yield 'b';

 yield 'c';

\[...abcs()\]; _// \['a', 'b', 'c'\]_

In the presentation there was a neat example about a French card deck object with the special property \[Symbol.iterator\] and the presenter used the fact that generators are also iterable so that when we spread the deck object, the internal iterator of the object, which is a generator function, creates all the French deck cards. This presentation helped us to **think out-of-the-box about generators and their practical uses in our applications**.

[Here](https://youtu.be/gu3FfmgkwUc) you can watch the full presentation.

**Typed JavaScript? For Real? The “Type Annotations” Proposal and What It’s All About by Gil Tayar**

Gil presented a TC39 proposal on including types in vanilla JavaScript. The proposal currently is in the first stage, so anything can happen still, but the idea behind types in JavaScript is not uncommon—just think about TypeScript or Flow.

_But we have TypeScript!_ – you might think.

Yes, but the proposal aims to provide a **common alternative to TypeScript in which you don't necessarily have to transpile your code**.

The types would still be ignored by the runtime, similar to how TypeScript works, and the types would be applied by annotations with similar syntax to TypeScript.

Internally, we had an interesting conversation about this topic. In itself, this doesn't provide anything more than just using TypeScript. However, diversity is always welcome, and another option for typed JavaScript is, again, very good. We are very curious about how this proposal will evolve.

[Here](https://youtu.be/SdV9Xy0E4CM) you can watch the full presentation.

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2105876/7443" target="_top" id="2105876">
  <img src="//a.impactradius-go.com/display-ad/7443-2105876" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2105876/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### **Communicating Intention with Functional TypeScript by Thiago Temple**

This presentation by Thiago caught our attention for several reasons:

1. a) we use TypeScript extensively here at ABBYY;
2. b) let's face it, when it comes to typing, we developers can be lazy 😊

So hearing some advice, tips and tricks is always helpful. The “gotcha” moment for us in this presentation was to **put more focus on typing, not just for the positive scenario but for (controlled) failures as well**. I'm pretty sure all of you are familiar with code (pseudo) like this:

type Order = {...}

type OrderResult = Result<ProcessedOrder>

function processOrder(order: Order): OrderResult {}

The upper code is quite standard, but what if we throw from the function, or what happens if the order is null ? Maybe the function handles the missing input, in which case it returns a different result. Thiago reminded us to handle those edge-cases as well. Here is an example from the presentation:

type Order = {...}

type OrderResult = Result<ProcessedOrder, OrderProcessingError>

function processOrder(order: Order): OrderResult {}

The speaker also talked about using union types when the input for the function is a well-defined finite set of string values. One way this helps us is to catch typo errors. Here at ABBYY we use union types all the time, so it was nice to learn a little more about them.

[Here](https://youtu.be/fhyHgkH0ZEg) you can watch the full presentation.

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137224/26400" target="_top" id="2137224">
  <img src="//a.impactradius-go.com/display-ad/26400-2137224" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137224/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### **7±2 Reasons Psychology Will Help You Write Better Code by Moran Weber**

This was a really exciting talk, and I encourage all of you to watch the video and play along with the little “games”. Moran has a degree in social psychology along with a lot of experience in software development. She shared several cognitive psychology principles that help to better understand how we read and interpret code.

For example, it is common knowledge among developers to use meaningful naming of variables, functions, etc. We all know the requirements. But do we really understand why good naming yields better collaboration? While shamelessly I would reply “yes”, in reality I did not. This presentation explains and demonstrates this extremely well.

One other thing that sticks in my mind and that I have practiced with my team since the conference is that **code reviews should always be cold**. This means no design explanation and intro is needed before handing your code—just send out a pull request. Otherwise, we could fall into a selective attention trap and not stay objective while reviewing the code.

[Here](https://youtu.be/jAUcbFM0nXE) you can watch the full presentation.

### **Testing Web Accessibility by Adrián Bolonio**

Adrián spoke about web accessibility. At ABBYY Hungary we are working on a web application for ABBYY [Timeline](https://tools.techidaily.com/abbyy/products/)—a cloud-based process intelligence platform that helps companies improve their processes. The target audience does not include every day users rather, per se, superusers such as business analysts. We don't have to think about web accessibility (which is usually referred to as a11y), the target audience just does not require this, right? WRONG. And Adrián explains very well why my statement is so wrong.

According to the presenter, every web application should care about accessibility. It is so easy to consider a11y as something we have to think about only when the target audience includes people with disabilities. Well, what if I tell you this mindset is wrong, and we all should care about a11y regardless of the type of application we are making? Adrián showed us that not only disabled people might use our applications leveraging a11y capabilities, like screen readers or other aids, but people with temporary inconveniences may also need them. For example, a father having his kid on his lap (sounds familiar in the era of home office?) and being able to use the application with only one hand. Or a worker having some temporary eye strain, which can happen to any of us.

This talk was influential—I could even say eye-opening!—to many of us attending the conference. The presentation has given us **ideas and inspiration about the direction in which we want to develop the product we are working on**.

[Here](https://tools.techidaily.com/abbyy/products/) you can watch the full presentation.

\*_All presentations in the program were insightful, and we enjoyed each one of them. The upper excerpts reflect our team's best memories about the conference._

### **Conclusion**

For me, personally, this was the first JSConf I was able to attend here in Budapest. I felt the focus was more on the less technical aspects of web development rather than straight technical JavaScript, which was an advantage. This way topics like web accessibility and psychology could gain some love and attention. Huge thanks to the JSConf Budapest team for organizing the conference.

[Tech Talk](https://tools.techidaily.com/abbyy/products/) 

![](https://static4.abbyy.com/abbyycommedia/36306/attila-kling-88x88.png)

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1972698/19272" target="_top" id="1972698">
  <img src="//a.impactradius-go.com/display-ad/19272-1972698" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1972698/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

Attila Kling

Software Development Group Team Lead

Attila leads a software development group of ABBYY Timeline. His day-to-day job includes managing web development projects, and he has a keen interest in web-security, user-management, authentication, and authorization.

<!-- affiliate ads begin -->
<a href="https://bluettius.sjv.io/c/5597632/2139116/17108" target="_top" id="2139116">
  <img src="//a.impactradius-go.com/display-ad/17108-2139116" border="0" alt="https://techidaily.com" width="250" height="90"/>
</a>
<img height="0" width="0" src="https://bluettius.sjv.io/i/5597632/2139116/17108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

### Like, share or repost

Share 

#### Subscribe for blog updates

First name\*

E-mail\*

Сountry\*

СountryAfghanistanAland IslandsAlbaniaAlgeriaAmerican SamoaAndorraAngolaAnguillaAntarcticaAntigua and BarbudaArgentinaArmeniaArubaAustraliaAustriaAzerbaijanBahamasBahrainBangladeshBarbadosBelgiumBelizeBeninBermudaBhutanBoliviaBonaire, Sint Eustatius and SabaBosnia and HerzegovinaBotswanaBouvet IslandBrazilBritish Indian Ocean TerritoryBritish Virgin IslandsBrunei DarussalamBulgariaBurkina FasoBurundiCambodiaCameroonCanadaCape VerdeCayman IslandsCentral African RepublicChadChileChinaChristmas IslandCocos (Keeling) IslandsColombiaComorosCongo (Brazzaville)Congo, (Kinshasa)Cook IslandsCosta RicaCroatiaCuraçaoCyprusCzech RepublicCôte d'IvoireDenmarkDjiboutiDominicaDominican RepublicEcuadorEgyptEl SalvadorEquatorial GuineaEritreaEstoniaEthiopiaFalkland Islands (Malvinas)Faroe IslandsFijiFinlandFranceFrench GuianaFrench PolynesiaFrench Southern TerritoriesGabonGambiaGeorgiaGermanyGhanaGibraltarGreeceGreenlandGrenadaGuadeloupeGuamGuatemalaGuernseyGuineaGuinea-BissauGuyanaHaitiHeard and Mcdonald IslandsHoly See (Vatican City State)HondurasHong Kong, SAR ChinaHungaryIcelandIndiaIndonesiaIraqIrelandIsle of ManIsraelITJamaicaJapanJerseyJordanKazakhstanKenyaKiribatiKorea (South)KuwaitKyrgyzstanLao PDRLatviaLebanonLesothoLiberiaLibyaLiechtensteinLithuaniaLuxembourgMacao, SAR ChinaMacedonia, Republic ofMadagascarMalawiMalaysiaMaldivesMaliMaltaMarshall IslandsMartiniqueMauritaniaMauritiusMayotteMexicoMicronesia, Federated States ofMoldovaMonacoMongoliaMontenegroMontserratMoroccoMozambiqueMyanmarNamibiaNauruNepalNetherlandsNetherlands AntillesNew CaledoniaNew ZealandNicaraguaNigerNigeriaNiueNorfolk IslandNorthern Mariana IslandsNorwayOmanPakistanPalauPalestinian TerritoryPanamaPapua New GuineaParaguayPeruPhilippinesPitcairnPolandPortugalPuerto RicoQatarRomaniaRwandaRéunionSaint HelenaSaint Kitts and NevisSaint LuciaSaint Pierre and MiquelonSaint Vincent and GrenadinesSaint-BarthélemySaint-Martin (French part)SamoaSan MarinoSao Tome and PrincipeSaudi ArabiaSenegalSerbiaSeychellesSierra LeoneSingaporeSint Maarten (Dutch part)SlovakiaSloveniaSolomon IslandsSouth AfricaSouth Georgia and the South Sandwich IslandsSouth SudanSpainSri LankaSurinameSvalbard and Jan Mayen IslandsSwazilandSwedenSwitzerlandTaiwan, Republic of ChinaTajikistanTanzania, United Republic ofThailandTimor-LesteTogoTokelauTongaTrinidad and TobagoTunisiaTurkeyTurks and Caicos IslandsTuvaluUgandaUkraineUnited Arab EmiratesUnited KingdomUnited States of AmericaUruguayUS Minor Outlying IslandsUzbekistanVanuatuVenezuela (Bolivarian Republic)Viet NamVirgin Islands, USWallis and Futuna IslandsWestern SaharaZambiaZimbabwe

* I have read and agree with the [Privacy policy](https://tools.techidaily.com/abbyy/products/) and the [Cookie policy](https://tools.techidaily.com/abbyy/products/).

* I agree to receive email updates from ABBYY Solutions Ltd. such as news related to ABBYY Solutions Ltd. products and technologies, invitations to events and webinars, and information about whitepapers and content related to ABBYY Solutions Ltd. products and services.  
    
I am aware that my consent could be revoked at any time by clicking the unsubscribe link inside any email received from ABBYY Solutions Ltd. or via [ABBYY Data Subject Access Rights Form](https://tools.techidaily.com/abbyy/products/).

Referrer

Last name

Query string

Product Interest Temp

UTM Campaign Name

UTM Medium

UTM Source

ITM Source

GA Client ID

UTM Content

GDPR Consent Note

Captcha Score

Page URL

Connect with us

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://youtube-zero.techidaily.com/024-approved-how-to-increase-video-engagement-with-customizable-youtube-thumbnails/"><u>[New] 2024 Approved How to Increase Video Engagement with Customizable YouTube Thumbnails</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/updated-how-to-upgrade-your-stream-quality-obs-for-youtube-and-twitch/"><u>[Updated] How to Upgrade Your Stream Quality OBS for YouTube & Twitch</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/updated-in-2024-discoveries-await-5-essential-maps-for-richer-gameplay/"><u>[Updated] In 2024, Discoveries Await 5 Essential Maps for Richer Gameplay</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/ed-in-2024-selecting-premier-sound-editors-for-youtube-producers/"><u>[Updated] In 2024, Selecting Premier Sound Editors for YouTube Producers</u></a></li>
<li><a href="https://solve-helper.techidaily.com/cookiebot-enhanced-user-experience-boost-your-sites-performance/"><u>Cookiebot-Enhanced User Experience: Boost Your Site's Performance!</u></a></li>
<li><a href="https://solve-helper.techidaily.com/elevate-your-business-with-abbyy-webinar-on-seamless-data-management-and-analysis-skills/"><u>Elevate Your Business with ABBYY Webinar on Seamless Data Management and Analysis Skills</u></a></li>
<li><a href="https://solve-helper.techidaily.com/enhance-user-experience-and-retargeting-via-smart-cookie-technology-discover-cookiebot-solutions/"><u>Enhance User Experience & Retargeting via Smart Cookie Technology: Discover Cookiebot Solutions</u></a></li>
<li><a href="https://solve-helper.techidaily.com/enhance-user-experience-through-cookiebot-enabled-features/"><u>Enhance User Experience Through Cookiebot-Enabled Features</u></a></li>
<li><a href="https://solve-helper.techidaily.com/enhance-your-online-data-collection-with-the-advanced-capabilities-of-cookiebot-driven-solutions/"><u>Enhance Your Online Data Collection with the Advanced Capabilities of Cookiebot-Driven Solutions</u></a></li>
<li><a href="https://solve-helper.techidaily.com/enhancing-claims-management-with-abbyys-digital-expertise-at-ecclesia-gruppe-an-seo-optimized-approach-to-insurance-services/"><u>Enhancing Claims Management with ABBYY's Digital Expertise at Ecclesia Gruppe – An SEO-Optimized Approach to Insurance Services</u></a></li>
<li><a href="https://solve-helper.techidaily.com/enhancing-productivity-with-automated-bill-management-from-abbyy-key-driver-for-energy-companies/"><u>Enhancing Productivity with Automated Bill Management From ABBYY - Key Driver for Energy Companies</u></a></li>
<li><a href="https://fox-info.techidaily.com/fast-tracked-finesse-how-to-efficiently-edit-and-enhance-windows-photos/"><u>Fast-Tracked Finesse How to Efficiently Edit and Enhance Windows Photos</u></a></li>
<li><a href="https://solve-helper.techidaily.com/from-cartography-to-smart-data-the-surprising-link-between-map-books-and-advancing-process-intelligence-exploring-with-abbyy/"><u>From Cartography to Smart Data: The Surprising Link Between Map Books and Advancing Process Intelligence | Exploring with ABBYY</u></a></li>
<li><a href="https://techtrends.techidaily.com/from-novice-to-master-the-definitive-guide-to-playing-pokemon-go/"><u>From Novice to Master: The Definitive Guide to Playing Pokémon GO</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/seamlessly-moving-your-memories-a-guide-to-uploading-google-photos-into-icloud/"><u>Seamlessly Moving Your Memories: A Guide to Uploading Google Photos Into iCloud</u></a></li>
<li><a href="https://facebook-video-content.techidaily.com/the-ultimate-guide-to-upgraded-audio-increasing-pc-volume-seamlessly-with-windows-10/"><u>The Ultimate Guide to Upgraded Audio: Increasing PC Volume Seamlessly with Windows 10</u></a></li>
<li><a href="https://ai-video-apps.techidaily.com/updated-2024-approved-windows-8-avi-editor-a-simple-way-to-edit-and-enhance-videos/"><u>Updated 2024 Approved Windows 8 AVI Editor A Simple Way to Edit and Enhance Videos</u></a></li>
</ul></div>

