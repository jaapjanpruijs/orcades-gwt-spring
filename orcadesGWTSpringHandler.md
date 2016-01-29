# Introduction #

Very simple dispatcher, that need minimal(?) configuration.


# Details #

```
         <servlet>
                 <servlet-name>gwt-handler</servlet-name>
                 <servlet-class>org.springframework.web.context.support.HttpRequestHandlerServlet</servlet-class>
        </servlet>


        <servlet-mapping>
                <servlet-name>gwt-handler</servlet-name>
                <url-pattern>*.gwtrpc</url-pattern>
        </servlet-mapping>
```

request from `*`.gwtrpc are then dispatch to the first implementation of the GWT Requested service found in the managed beans.
Jist add in your spring context.

`<import resource="classpath:META-INF/net/orcades/gwt/spring/gwt-spring.xml" />`
This declare the gwt-handler bean.

Enjoy.