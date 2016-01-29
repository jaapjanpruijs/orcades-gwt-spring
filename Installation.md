# Introduction #

Thanks to maven, it's not a big issue ...
There a are just some dependencies to provide, because some project are not available yet in public/central repositories:


  * gwt-dispatch
  * gwt-presenter



# Build #

checkout the whole project.

cd projects/orcades-gwt-spring

To build eclipse metatdata (.project, .classpath and wtp descriptors )

`mvn eclipse:clean eclipse:m2eclipse`

Or launch the eclipse launch ( Run >> Run Configuration )

`orcades-gwt-spring-rebuild-eclipse-metadata`

To build and install in your repo:

`mvn clean install`

# Import project into eclipse #

To import and use those project your eclipse install must have:
  * svn support
  * maven support (m2eclipse)
  * webapp support (WTP)
  * GWT support (GEP)
  * Spring support (STS)

Just use :
File >> Import >> Maven existing project

Becarefull to import only leaf projects:
  * orcades-gwt-spring-handler
  * orcades-gwt-spring-dispatch
  * orcades-gwt-spring-dispatch-security
  * orcades-gwt-spring-demo

**Not** the parent project orcades-gwt-spring

<font color='red'><b>Important step</b></font>

To deploy GWT compilation file in WTP module:

In the project orcades-gwt-spring-demo

Edit the /orcades-gwt-spring-demo/.settings/org.eclipse.wst.common.component file:

add `<wb-resource deploy-path="/search" source-path="war/search"/>`

This WTP customization should be handled by an eclipse plugin to synchronize as soon as module are added remove ...