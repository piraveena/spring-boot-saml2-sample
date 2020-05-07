# spring-boot-saml2-sample

The sample application uses Spring Boot and the spring-security-saml2-service-provider module which is new in Spring Security 5.2. This shows how to integrate your spring-boot-saml application with WSO2 Identity Server

## Register an saml service provider

- The next step is to configure spring-boot-app as the service provider. The following steps instruct you on how to do
 this.

1. Start the Identity Server and access the management console using https://localhost:9443/carbon/
2. Log in to the Identity Server using default administrator credentials (the username and password are both "admin").
3. In the management console found on the left of your screen, navigate to the Main menu and click Add under Service
 Provider. 
4. Expand the Inbound Authentication Configuration section and then expand SAML2 Web SSO Configuration. 


| Field                 | Value         | 
| --------------------- | ------------- | 
| Service Provider Name | sampleapp  |
| Issuer                | http://localhost:8080/saml2/service-provider-metadata/wso2  | 
| Description           | This is a spring-boot application secured with SAML using WSO2IS | 
| Assertion Consumer URL| http://localhost:8080/login/saml2/sso/wso2   | 

![Sceenshot](assets/saml-inboud-config.png?raw=true)

## Reference
1. https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-external-config-yaml
2. https://github.com/spring-projects/spring-security/blob/master/docs/manual/src/docs/asciidoc/_includes/servlet/saml2/saml2-login.adoc

