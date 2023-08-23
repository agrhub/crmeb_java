How to build the installation file
1. Go to home project directory
2. Run cmd'mvn clean install "-Dgpg.skip=true" "-Dmaven.javadoc.skip=true" "-Dmaven.test.skip=true"' to build java projects with maven


# surroundings
1. Java Jdk1.8
2. Redis 5+
3. Mysql 5.7+

# Java project framework
1. SpringBoot 2.2.6.RELEASE
2. Maven 3.6.1
3. Swagger 2.9.2
4. Mybatis Plus 3.3.1


# Deployment
1. Get the jar package and upload it to the web directory (the web directory pointed to by the domain name of the pagoda configuration)
2. Run the `start.sh (run command is ./start.sh )` script in the same level directory of the jar package to start the project
3. The shell script will automatically run the `tail -f crmeb_out.file` command to output the current startup log
4. Seeing `Completed 200 OK` indicates successful startup
5. The port number of `20000` is activated by default

# Precautions
1. The web port number cannot be set to `20000`
2. Reverse proxy address: `http://127.0.0.1:20000` [The external network domain name points to this address]


# Secondary development help document
##Note reference:
1. `@NotNull` Annotation Action Type Explanation Any type attribute cannot be `null`
2. `@NotEmpty` set The set cannot be `null`, and `size` is greater than `0`
3. `@NotBlank` can only be used on `String`, it cannot be `null`, and after calling `trim()`, the length must be greater than `0`
4. `@AssertTrue` `Boolean, boolean` Boolean attribute must be `true`
5. `@Min` number types (atoms and packaging) limit the minimum value of numbers (integer)
6. `@Max` is the same as `@Min` to limit the maximum value of a number (integer)
7. `@DecimalMin` is the same as `@Min` to limit the minimum value of the number (string, decimal)
8. `@DecimalMax` is the same as `@Min` to limit the maximum value of a number (string, decimal)
9. `@Range` number type (atoms and packaging) limited number range (long integer)
10. `@Length` string limit string length
11. `@Size` collection limit collection size
12. `@Past` time and date must be a past time or date
13. `@Future` period, time must be a future time or date
14. `@Email` string must be an email format
15. `@Pattern` string, character regular match string

# Product Copy
1. Set the api corresponding to [99api](https://www.99api.com "99api") to the configuration table eb_system_config
2. Configure baseUrl and key. The actual key can be modified according to your own definition
3. Currently supports Tmall, JD, Taobao, Suning, Pinduoduo

# Printer
1. [EasyLink Cloud Document](http://doc2.10ss.net/337744 "EasyLink Cloud Document")
2. [Easy Link JAVA SDK](http://doc2.10ss.net/337744 "Easy Link JAVA SDK gitee document")
3. [How to import the third-party JAVA SDK package](https://blog.csdn.net/weixin_46028577/article/details/106342938?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase&depth_1-utm_source= distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase "How to import a third-party JAVA SDK package")