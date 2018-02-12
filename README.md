# BJSS-Tests
Front end and api tests for BJSS technical test

Tests 1 and 2

Any attempt to interact with elements on MyAccount page (http://automationpractice.com/index.php?controller=my-account) produced the following error:

Message: Unexpected error. System.Net.WebException: Unable to connect to the remote server ---> System.Net.Sockets.SocketException: No connection could be made because the target machine actively refused it 127.0.0.1:53153
   

From investigation of the problem online, I found the following:

""Actively refused it" means that the host sent a reset instead of an ack when you tried to connect. It is therefore not a problem in your code. Either there is a firewall blocking the connection or the process that is hosting the service is not listening on that port, this may be because it is not running at all or because it is listening on a different port."

I contacted support@seleniumframework.com, but at the time of writing I have not had any response.

Therefore I continued the remaining sections of the test, which I did get to work successfully.
I returned to tests 1 and 2 and completed the the best I could without any working system to test.
The automation code that I have written for these scenarios does build successfully and at least shows how I would have approached the problem if the SUT was working.

Test 4

My code for this requires Postman in order to view.

Tech Debt

Many of the fields (particularly in the My Account page) were very difficult to select because of the way the code was written. I had to therefore use less than perfect approaches to 
reach these elements. This may because the code is poorly written or perhaps on purpose to make the test more challenging. 

Several of the the APIs for Test 4 do not work as specified. I have put comments about this in the test themselves.


