# test
web
<context-param>
        <param-name>log4jConfigLocation</param-name>
        <param-value>/WEB-INF/config/log4j.xml</param-value>
    </context-param>
  <listener>

<listener>
        <listener-class>org.springframework.web.util.Log4jConfigListener</listener-class>
    </listener>
 
    
xml
    <?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">

<log4j:configuration xmlns:log4j="http://jakarta.apache.org/log4j/">

    <appender name="console" class="org.apache.log4j.ConsoleAppender">
        <param name="Threshold" value="DEBUG"/>
        <layout class="org.apache.log4j.PatternLayout">
            <param name="ConversionPattern"
                   value="[%p] [%d{dd-MM-yy HH:mm:ss}] %c{1}.%M(%L): %m%n"/>
        </layout>
    </appender>

<!--     <appender name="spring" class="org.apache.log4j.RollingFileAppender"> -->
<!--         <param name="Threshold" value="DEBUG"/> -->
<!--         <param name="File" value="C:/Users/ivan2/Desktop/logss/afores.log"/> -->
<!--         <param name="MaxFileSize" value="50000KB"/> -->
<!--         <param name="MaxBackupIndex" value="9"/> -->
<!--         <layout class="org.apache.log4j.PatternLayout"> -->
<!--             <param name="ConversionPattern"  -->
<!--                    value=" [sapi] %p [%d{dd-MM-yy HH:mm:ss}] (%C{1}.%M:%L)| %m%n"/> -->
<!--         </layout> -->
<!--     </appender> -->

<!--     <appender name="afore" class="org.apache.log4j.RollingFileAppender"> -->
<!--         <param name="File" value="C:/Users/ivan2/Desktop/logss/afores.log"/> -->
<!--         <param name="MaxFileSize" value="50000KB"/> -->
<!--         <param name="MaxBackupIndex" value="9"/> -->
<!--         <layout class="org.apache.log4j.PatternLayout"> -->
<!--             <param name="ConversionPattern"  -->
<!--                    value=" [sapi] %p [%d{dd-MM-yy HH:mm:ss}] (%C{1}.%M:%L)| %m%n"/> -->
<!--         </layout> -->
<!--     </appender> -->

	<appender name="afore" class="org.apache.log4j.rolling.RollingFileAppender">
	    <rollingPolicy class="org.apache.log4j.rolling.TimeBasedRollingPolicy">
	        <param name="ActiveFileName" value="C:/Users/ivan2/Desktop/logss/app.log" />
	        <param name="FileNamePattern" value="C:/Users/ivan2/Desktop/logss/app.%d{yyyyMMdd}.%d{HHmm}.log.gz" />
	    </rollingPolicy>
	    <triggeringPolicy
	        class="org.apache.log4j.rolling.SizeBasedTriggeringPolicy">
	        <param name="MaxFileSize" value="1014" />
	    </triggeringPolicy>
	    <layout class="org.apache.log4j.PatternLayout">
	        <param name="ConversionPattern" value="%d{yyyy-MM-dd HH:mm:ss} %-5p - %m%n" />
	    </layout>
	</appender>

<!--     <logger name="org.springframework" additivity="true"> -->
<!--         <level value="debug"/> -->
<!--         <appender-ref ref="spring"/> -->
<!--     </logger> -->
  
    <logger name="mx.com.aforebanamex" additivity="true">
        <level value="all"/>
        <appender-ref ref="afore"/>
    </logger>

    <root>
        <level value="debug"/>
        <appender-ref ref="console"/>
    </root>

</log4j:configuration>
