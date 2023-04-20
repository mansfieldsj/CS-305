# CS-305

    • Briefly summarize your client, Artemis Financial, and their software requirements. Who was the client? What issue did they want you to address? 
	
The client Artemis Financial is a consulting company that specializes in personal financial plans. They were developing a RESTful web application using the Spring framework and hired us to analyze their software from a security standpoint and recommend changes in order to make sure that their client’s data and their data was secure with this application. We needed to address coding best practices, dependency vulnerabilities, implement secure communication and implement a checksum to verify secure communication.
	
    • What did you do very well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall wellbeing? 

The part that came easily to me and that I did very well was to mitigate dependency vulnerabilities by way of updating the dependencies used. As most software is upgraded on a regular basis, a large portion of those upgrades are strictly for security reasons. There is no reason not to use the latest versions of code especially when personal/financial data is in question. After I updated the dependencies and ran a second Maven check, there was still another dependency that was vulnerable but also wasn’t the latest version. I had to add an entry to pom.xml to update this and then ran the Maven check again to reveal no dependency vulnerabilities. We often have to rely on other people’s code to run our code however we do not have control over the other’s code, in this case it is that much more important that we use their latest versions to make sure it is as secure as possible.

    • What part of the vulnerability assessment was challenging or helpful to you? 

One aspect of the vulnerability assessments we conducted that was challenging for me was the visual code assessment. Coming into these assignments, my understanding of Java was minimal. Because of this, it was somewhat hard to determine what code was using secure best practices just by looking at it. Being exposed to it though did help with familiarity for the future.

    • How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use? 

Other than upgrading dependencies, I also increased layers of security by implementing a self-signed certificate in order to implement  secure communication (HTTPS). On top of that I used an appropriate cipher to verify the connection by way of a checksum. In the future I would use the same techniques as laid out here, however if this were an actual project that would be public, the use of a self-signed CA should not be used as it is vulnerable as well. In this case the company should pay for a legitimate third party CA for security reasons.

    • How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities? 

After refactoring the code I ran it to make sure there were no errors. I also opened the connection in the web browser, this showed me that the cipher was functioning as well as the self-signed certificate. Lastly I ran a final Maven check to verify that the dependencies were free of vulnerabilities.

    • What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks? 

All of the tools laid out above were helpful for these assignments as well as would be helpful in the future. The only change I wish for the future would be for me to be more familiar with the code I am assessing.

    • Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

I would be able to show future employers my ability to mitigate dependency vulnerabilities, my understanding and ability of implementing web certificates, and my understanding and ability to implement hash ciphers and checksums.
