# cs372-project-4---client-server-chat-solved
**TO GET THIS SOLUTION VISIT:** [CS372 Project 4 – Client / Server Chat Solved](https://www.ankitcodinghub.com/product/cs372-project-4-client-server-chat-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;95800&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS372 Project 4 – Client \/ Server Chat Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

Introduction

In this coding project you will write a simple client-server program using python sockets. Your program will emulate a simple chat client. For extra-credit (points tbd), turn your chat program into a simple ascii multiplayer game (see below for spec).

Writing a client-server socket program

This chat client-server is fairly simple in design. The server doesn’t handle multiple clients, and there is only one socket connection made. You will reuse this socket for the life of the program. The one issue with reusing sockets is that there is no easy way to tell when you’ve received a complete communication:

“… if you plan to reuse your socket for further transfers, you need to realize that there is

no EOT (end of transmission) on a socket. I repeat: if a socket send or recv returns after handling 0 bytes, the connection has been broken. If the connection has not been broken, you may wait on a recv forever, because the socket will not tell you that there’s nothing more to read (for now). Now if you think about that a bit, you’ll come to realize a fundamental truth of sockets: messages must either be fixed length (yuck), or be delimited (shrug), or indicate how long they are (much better), or end by shutting down the connection. The choice is entirely yours, (but some ways are righter than others).”

Source: https://docs.python.org/3.4/howto/sockets.html

There are several ways around this, including simply specifying a different port every time you run. A good alternative, that mostly works, is to set a socket reuse option before the bind command on the server: s.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)

Specification

Server

<ol>
<li>The server creates a socket and binds to ‘localhost’ and port xxxx</li>
<li>The server then listens for a connection</li>
<li>When connected, the server calls recv to receive data</li>
<li>The server prints the data, then prompts for a reply</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
Note that in the process of testing, you can “hang” a port. This will give an error when you start the server: [Errno 48] Address already in use. Don’t worry, the ports will recycle eventually.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ol start="5">
<li>If the reply is /q, the server quits</li>
<li>Otherwise, the server sends the reply</li>
<li>Back to step 3</li>
<li>Sockets are closed (can use with in python3)</li>
</ol>
Client

<ol>
<li>The client creates a socket and connects to ‘localhost’ and port xxxx</li>
<li>When connected, the client prompts for a message to send</li>
<li>If the message is /q, the client quits</li>
<li>Otherwise, the client sends the message</li>
<li>The client calls recv to receive data</li>
<li>The client prints the data</li>
<li>Back to step 2</li>
<li>Sockets are closed (can use with in python3)</li>
</ol>
A better spec might just be to show example screenshots:

What to turn in

<ol>
<li>In the Word doc:
<ol>
<li>Include instructions on how to run your programs. Are they python3?</li>
<li>Include screenshots of your running code.</li>
<li>Include comments / questions (optional)</li>
</ol>
</li>
<li>In your code listings:
<ol>
<li>Include sources you used (web pages, tutorials, books, etc)</li>
<li>Comment your code</li>
</ol>
</li>
</ol>
Extra Credit

Turn your client-server into a multiplayer ascii game. Tic-tac-toe? Hangman? The choice is up to you. Points awarded subjectively based on effort. 5 extra points possible.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Resources

https://docs.python.org/3.4/howto/sockets.html https://realpython.com/python-sockets/

</div>
</div>
</div>
