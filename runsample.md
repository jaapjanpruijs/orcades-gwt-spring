# Introduction #

orcades-gwt-spring-demo project hold a sample application.
With spring dispatcher using spring security at method level.


There are some issues with Spring namespacehandler ant GWT Hosted (Dev) mode (http://groups.google.com/group/google-web-toolkit/browse_thread/thread/be6b6681192aa54a?pli=1)


When the server side code is not using the embeded jetty server, it's ok.


# Details #

Launch the GWT compilation with GEP. (refresh workspace after).

Ensure that in the Maven dependencies are checked in

Project properties >> JEE Module dependencies

Then you should able to deploy the application has a wtp module.

  * Start your WTP server instance.

  * The start the (GEP) gwt module without the embeded server.
launch config: `orcades-gwt-spring-demo-noserver`

And thats it you should be able to access to
  * http://localhost:8080/orcades-gwt-spring-demo/search.html to use the compiled code.
  * http://localhost:8080/orcades-gwt-spring-demo/search.html?gwt.codesvr=127.0.0.1:9997 to use the dev mode.


Enjoy