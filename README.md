# test


log4j.appender.STDOUT=org.apache.log4j.ConsoleAppender
log4j.appender.STDOUT.Target=System.out
log4j.appender.STDOUT.layout=org.apache.log4j.PatternLayout
log4j.appender.STDOUT.layout.ConversionPattern=<CG><%d{yyyy-MM-dd HH:mm:ss}>[%-5p] %c - %m%n

log4j.appender.FILE=org.apache.log4j.rolling.RollingFileAppender
log4j.appender.FILE.rollingPolicy=org.apache.log4j.rolling.TimeBasedRollingPolicy
log4j.appender.FILE.rollingPolicy.ActiveFileName=C:/Users/ivan2/Desktop/logss/app.log
log4j.appender.FILE.rollingPolicy.FileNamePattern=C:/Users/ivan2/Desktop/logss/app.%d{yyyyMMdd}.%d{HHmm}.log.gz
log4j.appender.FILE.triggeringPolicy=org.apache.log4j.rolling.SizeBasedTriggeringPolicy
log4j.appender.FILE.triggeringPolicy.MaxFileSize=1014
log4j.appender.FILE.layout=org.apache.log4j.PatternLayout
log4j.appender.FILE.layout.ConversionPattern=<CG><%d{yyyy-MM-dd HH:mm:ss}>[%-5p] %c - %m%n

#log4j.appender.FILE=org.apache.log4j.RollingFileAppender
#log4j.appender.FILE.File=C:/Users/ivan2/Desktop/logss/afores.log
#log4j.appender.FILE.MaxFileSize=1KB
#log4j.appender.FILE.MaxBackupIndex=10
#log4j.appender.FILE.layout=org.apache.log4j.PatternLayout
#log4j.appender.FILE.layout.ConversionPattern=<CG><%d{yyyy-MM-dd HH:mm:ss}>[%-5p] %c - %m%n
#log4j.appender.FILE.append=true

log4j.rootLogger=INFO,FILE,STDOUT
log4j.logger.org.springframework=INFO,STDOUT
log4j.logger.mx.com.aforebanamex.plata=STDOUT
