---
layout: post
title: "Spring Boot"
date: 2020-01-23 10:22:33 +0900
categories: SpringBoot Start
---

command + shift + P 후 Spring Initializr 클릭
-> java, package,폴더명, spring 버전 선택

pom.xml 에

<dependency>
            <groupId>org.apache.tomcat.embed</groupId>
            <artifactId>tomcat-embed-jasper</artifactId>
            <scope>provided</scope>
</dependency>
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>jstl</artifactId>
            <scope>provided</scope>
        </dependency>
추가함(tomcat, jstl 사용설정)

application.properties 삭제 후
아래와 같이 application.yml 파일 추가
spring:
http:
encoding:
charset: UTF-8
mvc:
view:
prefix: /jsp/
suffix: .jsp
server:
tomcat:
uri-encoding: UTF-8
