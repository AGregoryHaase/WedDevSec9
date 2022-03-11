<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="CSSsection9.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
    <title>Section 9: <br>
        Other assorted Useful CSS Properties <br>
    </title>
</head>
<body>
    <h1 id="top">
        Section 9: <br>
        Other assorted Useful CSS Properties <br>
    </h1>
    <h2>In this section</h2>
    <section>
    <ul>
        <li><a href="#nine.91">91. What matters in this section</a></li>
        <li><a href="#nine.92">92. Opacity &amp; The Alpha Channel</a></li>
        <li><a href="#nine.93">93. The Position Property</a></li>
        <li><a href="#nine.94">94. CSS Transitions (yay!)</a></li>
        <li><a href="#nine.95">95. The Power of CSS Transforms</a></li>
        <li><a href="#nine.96">96. Fancy Button Hover Effect CodeAlong</a></li>
        <li><a href="#nine.97">97. The Truth About Background</a></li>
        <li><a href="#nine.98">98. Google Fonts is Amazing</a></li>
        <li><a href="#nine.99">99. Photo Blog CodeAlong pt. 1</a></li>
        <li><a href="#nine.100">100. Photo Blog CodeAlong pt. 2</a></li>
    </ul>
</section>
<hr>
<h2 id="nine.91">91. What matters in this section</h2>
<section>
    <ul>
        <li>CRUCIAL!</li>
            <ul>
                <li>Transitions</li>
                <li>Position Property</li>
            </ul>
        <li>IMPORTANT</li>
            <ul>
                <li>Opacity &amp; Alpha Channel</li>
                <li>Google Fonts</li>
                <li>The Full Story On the Background Property</li>
            </ul>
        <li>NICE TO HAVE</li>
            <ul><li>Transforms</li></ul>
    </ul>
</section>
<hr>

<h2 id="nine.92">92. Opacity &amp; The Alpha Channel</h2>

        <section class="wwiw">
            <div id="rgba">Right, I'm not too sure about this one. In this block we used RGBA, which looks like rgba(255,255,255,0.5).
                rgba stands for red green blue, which you probably know, and the a is alpha. THe alpha range is between 0 and 1 and defines the opacity of the colour. However, there is another way to define 
                opacity, which I will use in the block below. NB: Using rgba changes the colour of only the element it is applied to.
            </div>
            
        </section>
        <section class="wwiw">
            <div id="opac">Here we have used the opacity element. Again it is between 0 and 1. I'm not sure where the colour for the test is coming from.
                It seems to be inheriting the colour from the parent section (I think I now understand this as ) 
                <em>OKay, so basically what happens with the opacity tag is that it makes everything have the selected colour underneath.</em>
                Soeven this <button>button</button> should have the magenta colour coming through from behind.
            </div>
    
</section>
<hr>
<h2 id="nine.93">93. The Position Property</h2>
<section>
Generic sounding and the name doesn't tell you a lot. HE says a lot of students ahve to refer to the docs for help with this. 
Posiiton sets how an element is positioned in a document. 
THe top, right, bottom, left determine the final location of positioned elements.
here are the <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position" target="blank">MDN docs</a>
</section>
<p>OKay, so he sets up the following...</p>
<section class="static">
    <h2>static</h2>
    <p><em>the element is positioned according to the normal flow of the document. The top, right, bottom, left, and z-index properties have <u>no effect.</u>  
        THis is the default value. 
    </em></p>
    <div> </div>
    <div id="middle"></div>
    <div></div>
</section>
    <p>OKay so we created a style under .static #middle and then put in position: static;
        He then adds in top: 100px; and shows us that nothing happens because we have the position set to static.
        He then copy and pastes this section. but changes the id and class. Wait, I didn't change the ID I just had to change the class. 
        The class is still 
    </p>
    <h2><em>relative</em></h2>
    <em>The element is positioned according to the normal flow of the document and then offset <u>relative to itself</u>
       based in the values of top, right, bottom, and left. The offsett does not affect the position of any other elements; thus, 
       the space given for the element in the page layout is the same as if the position were static. 
    </em>
    <section class="relative">
        <div></div>
        <div id="middle"></div>
        <div></div>
    </section>
    <p class="overlap">OKay, so now that he's set this new relative section he goes on to say that he can now add top, 
        right, middle, bottom and left.
        He sets top to 100px which has dropped the box down. I've given the box opacity of 0.5 so that I can see the text through the box. 
        Nice bit of problem solving. 
        I guess I could add margin to the paragraph. That would probably be the best thing to do if I didn't want it all to overlap. 
        <EM>I'VE ACTUALLY Just added a margin of 100px to this paragraph with class 
            overlap which has moved the text down enough to not overlap with the box.
            however, I wonder if there is a more responsive way of doing this? 
            So when I moved the inspect window inwards and shrank this file window, 
            the text stayed the same distance to the box <u>until</u> the boxes were pushed 
            out of formation. At which point the boxes seemed to collapse into each other. 
            The gap to this text increased.
            I think I would have to add padding and margin to to the boxes? 
            Or maybe we're about to find out with this position thing.
        </p>
            <p>
                Anyway, he goes on to show how to move the block around using left and negative numbers. 
                He reminds us that even though he's put left: 100px; it will offset to the right. 
                It pushes it to the opposite direction. He also shows that you can use negative numbers and percentages.

                <p>next we look at <em>absolute</em></p>
            </p>
        </EM>
        
        <h2>absolute</h2>
            <a href="https://www.youtube.com/watch?v=2JMGG_8T-vY" target="blank">good vid here by net ninja</a>
            <p><em>   In the video he explains that you can set the position to of the parent to relative (let's say a banner) and then have the child (let's say a header) at say top: 30px; (down from top of the banner ).
            You could then put the child width at 100%. THis will be set relative to the banner. You can then put text align to center. This will create a header in a set position relative to the banner.
            Let me see if I can replicate it</em></p>
                
            <div class="banner">
                <h2>banner</h2>
                <p class="bannerp">Okay, so I've created the blue banner above. Now I'm going to try and move the header to the middle of it. 
                    first of all he does something pretty cool with controlling the banner. 
                    He adds a - max-height of 300px, and - overflow: hidden; and - margin:1%; to the banner.
                    HE then adds .banner h2 = position:absolute; plus top: 0; and left: 0;
                    The h2 header then jusmps to the top corner of the page, he then puts the parent as relative and the header then jumps to it's relative position on the banner, inside the banner.
                    He then adds width: 100%; to the h2 header and also text align: center;
                    THat's cool, it's worked properly. REally good video.
                    OKay so if I want to move this paragraph into the banner. I would wrap the paragraph in the .banner div, 
                    then go into the css and create .banner p  position: absolute; then add in top: 50px; and centre the text?
                    Let's give it a go. 
                    Okay, cool, did it!
                </p></div>

                <section class="fixed">
                    <h2 class="fixedh2">FIXED</h2>
                    <p>Right, so I'm going to attempt to do the NetNinja nav bar and also the fucking thing on the WDB with Colt.
                        Fucking, really struggling to think straaight. Ha. I like straaight spelt like that. 
                        Straaight. 
                        Fuck, okay. focus. 
                        Right, so let's start with Colt. 
                        He starts off by creating another set of divs, this time the central div has an id of fixed.
                        HE then goes into the CSS and creates a style for .fixed #middle with a position: fixed; and top: 0; left: 0;
                        OKay, I've done that. I'd like to add some text into the box that is fixed at the top of the screen though. How do I do that?
                        DUh! You just put it in the div, silly.
                        I ADDED IN A home button. I could put back to top on there probably.
                        Yep, I just did that. The fixed box is now a "back to top" button
                    </p>
                    <h3>WDB COLT's fixed example (I made it into the back to top box)</h3>
                    <div></div>
                    <div id="middle"><button><a href="#top">back to top</a></button></div>
                    <div></div>
                    </section>
                    <section class="netninjanav">
                        <h2>net ninja fixed nav bar</h2>
                        <div class="netfixedp"><p>
                            Okay, so we're doing the fixed position on net ninja. 
                            Find the video <a href="https://www.youtube.com/watch?v=8fQWx-d5qc8" target="blank">here</a>
                            first of all he creates the nav, ul, li with the text "link" inside.
                            He then adds CSS styles of nav li {list-style-type: none; and margin:0 10px;}
                            <p>setting the style to non gets rid of the dots. He then styles the nav with a background colour of #333, padding of 5px.
                                he then goes back to the li styling and adds in colour #fff and float: right;
                                okay so when you add in the float:right; it makes the links all collapse. He says this is becasue we haven't cleared the float.
                                I'm not sure what that means just yet. <em>look up what clearing the float and float in general are</em>
                                Okay, so he goes on to create styles for the nav ul, in my case it is the class nnnav ul. 
                                He adds in a psudo class:after so for me that will look like nnnav ul:after he types in content with an empty string ""
                                gives a display tag of block (display:block;) and then (clear:both)
                                So then we are going for <br>
                                nnnav ul:after <br>
                                    content:"";    
                                    display: block; <br>
                                    clear: both; <br>   
                                He says that this will restore the nav bar. Let's see. Nope, It didn't work.
                                Oh, I forgot the content and empty string. 
                                Okay, i missed a couple of things. but sorted it out quite quickly. 
                                Right, so to get it to be fixed to the top, you guessed it, we use position: fixed. 
                                So he goes into the nav, for me it'll be .nnnav class. He adds in <br> 
                                top: 0; <br> 
                                left: 0; <br> 
                                and <br> 
                                width:100%; <br>
                                Okay, that has all worked. I moved the fixed "back to top" button down 80% and gave it 50% opacity. That way it isn't in the way of the nav bar. 
                                One problem is that the nav bar covers the h1 header. I've made the nav bar 50% opaque but I need to figure out how to move that down. 
                                <em>cool, i got a nav bar</em>
                                Quite a lot went into that so I'll have to recap it soon.
                            </p>

        
                        </p></div>
                    <nav class="nnnav">
                        <ul>
                            <button id="hovbutt">HOVER ME</button>
                            <button id="hovbutt">HOVER ME</button>
                            <button id="hovbutt">HOVER ME</button>
                            <li id="hovbutt">link</li>
                            <li id="hovbutt">link</li>
                            <li id="hovbutt">link</li>
                         
                        </ul>
                    </nav>
                </section>
                    <hr>
                    <section class="sticky">
                        <h2>STICKY</h2>
                        <p>Okay, colt mentions this but says he's not going to go into it. 
                            I quite like the look of it though so I'm gonna give it a go.
                            Basically when something is defined as sticky it will act as fixed once it has been scrolled past. 
                            let me see if I can create one.
                            right, so I created one. I fucked up a little but only becasue I'd forgotten to close the previous section tag. 
                            It's sort of working now but it covers over the stuff below which is annoying (when it sticks)3
                        </p>
                        <div></div>
                        <div id="middle"><em>this is a sticky box of joy</em></div>
                        <div></div>
                        <p>OKay, so I can't quite get this to work properly yet. 
                            The only way I can sort of get it to work is when I add some text to this div. 
                            THe box is offset and seems to be inheriting the 90% right from the fixed cube css style above. 
                            Anyway, I'll have to come back and look at this another time because I want to move on. 
                            I'm stuck on sticky. NOw let me try and do the Net NIja fixed nav bar. 
                            Okay, so I sort of got it to work.
                            I want it to start from the same level as the other boxes, but it just won't at the moment. 
                            Maybe it's inheriting something from somehwere else, IDK.
                            I've given it a .5 opacity so that we can see what is underneath it. 
                            </p>
                    </section>
                    
                    
<hr>
<article class="article">
<h2 id="nine.94">94. CSS Transitions (yay!)</h2>
<p>OKay, so this is quite a difficult section. It's probably the hardest section I've done so far. 
    <br> I've done some examples below but I'm definitively not 100% on it and it's all looking a bit messy. 
    <br>I think maybe I need to create a whole other file for this section alone and then maybe add it 
    in to this page later. I did that. <br>
    First though, let me just see if I can add something in here. Then I really need to look at 
    that property mark thing tbh (I still haven't). 
    <aside>
        Cool, so this is the second time around doing this. I did it a week ago and then I've been back over 
        section 8 and through the first part of this section, up to this point.
        Cool. So, second time around. Moderately excited to be doing these again. 
        It'll be interesting to see what I can 
        create, I mean, see if I can create anything more advanced than last time.
        I've decided to start over again at the bottom of this article. This article will have a green background. 
        Below this article I'll start the 94 again.
    </aside>
    <aside class="tester">
        <div>ease in</div>
        <div>ease out</div>
        <div>ease in out</div>
        <div>ease in</div>
        <div>ease in</div>
        <p>
            Okay, so I got this to move but not to transition colour. How do I do that?
            <br>Cool, figured that out. 
            <br>Good resource for easings <a href="https://easings.net/" target="blank">here</a>
        </p>
    </aside>
</p>
<section>
    <h3>USING CSS TRANSITIONS</h3>
    <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions">Here is a Link to the MDN page</a>
<table>
<tr>
    <thead colspan="4"></thead>
    <td>TRANSITIONS</td>
</tr>
<tr>
    <td>property name</td>
    <td>duration</td>
    <td>timing function</td>
    <td>delay</td>
</tr>
</table>
<h3>transitions</h3>
<ul>
    <li>property name</li>
    <li>duration</li>
    <li>timing functin</li>
    <li>delay</li>
</ul>

    <div class="circle"></div>
    Here is a simple example of a transition when hovered over between shape and colour. 
    we do this with: <br>
    1) the above div set with a class. <br>
    2) we then add CSS style elements using that class to create width, height, color, radius, transition. <br>
    Here we will also set what will be transitioned to when hovered<br>
    .circle {<br>
    &nbsp;  width: 300px; <br>
            height:300px;<br>
            background-color: rgba(240, 101, 238, 0.88); <br>
            transition: background-color 1s, border-radius 2s; <br>
    } <br>
    .circle:hover { <br>
        background-color: cyan;<br> <!-- changes background color on hover -->
        border-radius: 0%;
    } <br>
    <article>
    <div class="circle2"></div>
</article>
    <section class="move">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</section>
<h3>TIMING FUNCTION</h3>
<p>
    There are many ways to go from red to blue in three seconds. Do we go really quickly in a linear fashion or do we start slow and then speed up or vice versa? <br>
    See this MDN sheet for more <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function">here</a> <br>
    this is specified as a <em>transition-timing-function</em> 
    <h4>transition-timing-function</h4>
    here are a few <br>
    <ul>
        <li>transition-timing-function: ease;</li>
        <li>linear</li>
        <li>ease-in</li>
        <li>ease-out</li>
        <li>ease-in-out</li>
        <li>cubic-bezier</li>
        <ul>    <li>found quite a cool resource for this here <a href="https://cubic-bezier.com/#0,.66,.35,.75" target="blank">nice!</a></li></ul>
        <li>steps</li>
        <li>jump-start</li>
        <li>jump-end</li>
        <li>jump-none</li>
        <li>jump-both</li>
        <li>start</li>
        <li>end</li>
        <li>step-start</li>
        <li>step-end</li>
    </ul>
</p>
<h4>transition-timing-function <br>
<em>ease</em></h4>
<!-- <aside>.move2:hover div { <br>
    background-color: silver; <br>
    border-radius: 50%; <br>
    margin-left: 100px; <br>
    transition: 2s; <br>
} <br>
div:nth-of-type(1) { <br>
    transition: ;
}</aside> -->
<section class="move2">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
</section>
<section class="test2">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
</section>
</article>
<hr class="specialhr">
<article class="article2">
    <h2>94. CSS Transitions (again)</h2>
<section>
    <p>Okay, so I've already done the CSS. It's for .circle3. So I think now I just have to create a div with a class of .circle3</p>
    <div class="circle3"></div>
    <div class="circle3"></div>
    <div class="circle3"></div>
    <div class="circle3"></div>
    <div class="circle3"></div>
    <div class="circle3"></div>
    <br>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <div class="circle4"></div>
    <p>Okay, so these circles just have the change of colour on hover. 
        Let me make another set where it changes froma  square to a circle</p>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <div class="circle5"></div>
        <p>THese last set of orange squares to green circles contain no transitions. 
            It is an instant change. Let's set up some transitions on another set of shapes.
            okay so for the circle6 blocks below, it has inherited some transitions which actually create a really cool effect that I want to 
            recreate for all of the blocks. So I'll try and do that now.
            It seems that we put the transition into the initial styling and not the psuedo tag of hover.
            <p>RIght, so I've added in a 2 second transition to the circle 6 class. However, the first few shapes are still inheriting a transition back 
                to the original shape, which is really nice. The others just instantly jump back to the original shape which looks jerky. 
                Super Jerk.
                Okay, so actually they should be transitioning back slowly. I'll have to look at the console to see where it is inheriting from.
                <p>wicked! I actually managed to see a problem and then go into the console and inspect the code. I think that's the right way of saying it. 
                    I managed to see where the style was being inherited from. 
                    I was also able to see that I had put the transition into the :hover and not the original style. That is what was causing the block to revert back instantly. 
                    <em>COOL BEANS</em>
                </p>
                <p>OKay SO I have jsut gone back through the old code and made some adjustments. It's all running smoothly now, except for the one rotate issue with the
                    first circle. I'll sort it out when we cover that section agian.
                </p>


            </p>
            
        </p>
        <article class="circle6art">     
        <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
            <div class="circle6"></div>
        </article>     

        
        <article class="blackart">
            <h3>Transition: Property Name | Duration | Timing Function | Delay</h3>
            <p>
                OKay so he starts of by saying that the transition: doesn't just have to have a time (5s)
                You can also have <ul>
                    <li>Property Name</li>
                    <li>Duration</li>
                    <li>Timing Function</li>
                    <li>Delay</li>
                </ul>
            </p>
            <h4>Property Name</h4>
            <p> Below I've recreated a similar version of the circle that colt creates. He changes the style to transition: background-color 3s;
            So the colour changes slowly but the shape changes instantly.
                Colt then shows us a delay on the color change and I've added that in to the below circles.
                Major tip here, you can also say transition: all 5s;
                I've take off the delay.
            </p>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <div class="propname"></div>
            <p>here's propname2</p>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
            <div class="propname2"></div>
        </article>
        <article class="redart">
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>
            <div class="trantimfunc"></div>   

        </article>

</section>

</article>
<hr>
<h2 id="nine.95">95. The Power of CSS Transforms</h2>
<section>
    <p>
        Hello there. We are now on to the <em>Power</em> of <em>transform</em>
        Colt goes ahead and makes a load of h1s with different colours with the text "transform me"
                </p>
                <p>HEre we learn a new way to centre elements on the page. MArgin: auto.
                    He says if we block level left and right margin to be auto it'll 
                    automatically evenly distribute the space in the container, either side of the element
                    he keeps margin: 20px but adds auto after this, so - margin:20px auto;
                </p>
                <h4>different types of transform</h4>
                <ul>
                    <li>martrix</li>
                    <ul><li>transform: matrix(1, 2, 3, 4, 5, 6)</li></ul>
                    <li>translate</li>
                    <ul><li>transform: translate (120px, 50%)</li></ul>
                    <li>scale</li>
                    <ul><li>scale(2, 0.5)</li></ul>
                    <li>rotate</li>
                    <ul><li>transform: rotate(0.5turn)</li></ul>
                    <li>skew</li>
                    <ul><li>skew(30deg, 20deg)</li></ul>
                    <li>shorthand transform: scale(0.5) translate(100%, 100%)</li>
                </ul>
                <p>see <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function">here for MDN page on transforms</a></p>
            <article class="transform">
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
            </article>
            <article class="transform">
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
                <h1>TRANSFORM ME</h1>
            <h3>some skews</h3>
            </article>
            <article class="divtrans">
                <div></div>
                <div></div>
                <div></div>
                <div></div>
                <div></div>
            </article>
        
    <h3>transform: Rotate</h3>
    <h3>transform: Scale</h3>

</section>
<hr>
<section>
    
        <h2 id="nine.96">96. Fancy Button Hover Effect CodeAlong</h2>

    <p>OKay, this section actually looks pretty cool. It'll be a nice effect to learn.</p>
    <article class="hoverme">
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
        <button id="hovbutt">HOVER ME</button>
    </article>
    <p>To add the box shadow. Go here <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow">here, not there.</a> </p>
    <p>box-shadow: x offset y offset blur radius spread radius </p>
</section>
<hr>
<H2 id="nine.97">97. The Truth About Background</H2>
<section>

<div>
    <p>Okay, what is the truth about background? 
        New doc, add sec, h1, I am heading. Makes large section. w80% h800px, background color, centre with margin auto. 
        h1, font size 100px. 
        color white
        give an image instead of a colour to the background. Can set a gradient as background.
        Specify a URL path to where your image is. Get one from your website. 
        In CSS background-image: url("url here please")
    </p></div>
        <div class="image"></div>
        <p>
        Okay, well I can get the gradient image to work but not an actual image. I'm trying to link to an online image. 
        Maybe I should try an image that's on my comp.
        Bloody nora been trying to do this for over an hour now. 2 hours now. 
        It just won't show a fucking image. 
        Right, so it's about 4 hous later and I couldn't get the fucking thing to work for ages. 
        I literally just manage to do it. 
        googled mandlebrot images and then took a url off one of those, which worked. 
        I just want to know how to have two images ontop of each other and then reduce the opacity on the top image to allow the 
        bottom one to come through. MAybe I;ll try and do that tomorrow, or later today. 

        Okay, I finally did it. NOt the opacity thing. 
        Relook at background shorthand

</p>
</div>    
</section>
<hr>
<h2 id="nine.98">98. Google Fonts is Amazing</h2>
<section>
<p>
    we already looked at the font family property. If we want to change something as a font, we use font family. I then ahve to be careful with what font I use. 
    We want to use web-safe fonts. 
    One option we have is to include a font file as part of our document. You can buy them, download them but they're pretty expensive. Some charge for each time the page is loaded!
    Google font we can use for free. 
    He basically just gives us a demo and says it's really cool. 
    I didn't realise Roboto was so popular
    Okay, so you can embed by copying the link and CSS
    I've actually just been on the site. It's cool. FOund a cool font to use. 
    Press Start 2P
    It says to put the following into the head...look at the HTML as it's commented out.
    <br>Good Lord, I just changed the font and it makes so much difference! What an idiot I am to think that this was almost like a nothing kind of thing.
    <!-- <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet"> -->
</p>
</section>
<hr>
<h2 id="nine.99">99. Photo Blog CodeAlong pt. 1</h2>
<section>

</section>
<hr>
<h2 id="nine.100">100. Photo Blog CodeAlong pt. 2</h2>
<section>
    
</section>
</body>
</html>
