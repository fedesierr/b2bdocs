#CompanyApi
The VISA B2B Connect REST API allows developers to perform operations from a company or bank perspective.  The VISA B2B Connect API allows you to create and update profiles or retreive information that is relevant to you.

All URIs are relative to *https://sandbox.api.visa.com/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postaddCompany**](CompanyApi.md#postaddCompany) | **POST** /visab2bconnect/v1/companies | 
[**puteditCompany**](CompanyApi.md#puteditCompany) | **PUT** /visab2bconnect/v1/companies/{enterpriseId} | 




<a name="postaddCompany"></a>
#**postaddCompany**
> AddCompanypostResponse postaddCompany(body)



Onboard a company.

### Example
```java
import com.visa.developer.sample.company_api.*;
import com.visa.developer.sample.company_api.auth.*;
import com.visa.developer.sample.company_api.model.*;
import com.visa.developer.sample.company_api.api.CompanyApi;
import java.io.File;
import java.util.*;

public class CompanyApiExample {

    public static void main(String[] args) {

        ApiClient apiClient = new ApiClient();

        // Configure HTTP basic authorization: basicAuth
        apiClient.setUsername("YOUR USERNAME");
        apiClient.setPassword("YOUR PASSWORD");
        apiClient.setKeystorePath("YOUR KEYSTORE PATH");
        apiClient.setKeystorePassword("YOUR KEYSTORE PASSWORD");
        apiClient.setPrivateKeyPassword("YOUR PRIVATEKEY PASSWORD");
        
        // To set proxy uncomment the below lines
        // apiClient.setProxyHostName("proxy.address@example.com");
        // apiClient.setProxyPortNumber(0000);

        CompanyApi apiInstance = new CompanyApi(apiClient);
        
        AddCompanypostPayload body = new AddCompanypostPayload(); // Set all the required parameters. Refer to the model documentation below for further information
        
        try {
            AddCompanypostResponse result = apiInstance.postaddCompany(body);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CompanyApi#postaddCompany");
            e.printStackTrace();
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AddCompanypostPayload**](AddCompanypostPayload.md)|  |


### Return type

[**AddCompanypostResponse**](AddCompanypostResponse.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


<a name="puteditCompany"></a>
#**puteditCompany**
> EditCompanyputResponse puteditCompany(body, enterpriseId)



Edit the information for a company.

### Example
```java
import com.visa.developer.sample.company_api.*;
import com.visa.developer.sample.company_api.auth.*;
import com.visa.developer.sample.company_api.model.*;
import com.visa.developer.sample.company_api.api.CompanyApi;
import java.io.File;
import java.util.*;

public class CompanyApiExample {

    public static void main(String[] args) {

        ApiClient apiClient = new ApiClient();

        // Configure HTTP basic authorization: basicAuth
        apiClient.setUsername("YOUR USERNAME");
        apiClient.setPassword("YOUR PASSWORD");
        apiClient.setKeystorePath("YOUR KEYSTORE PATH");
        apiClient.setKeystorePassword("YOUR KEYSTORE PASSWORD");
        apiClient.setPrivateKeyPassword("YOUR PRIVATEKEY PASSWORD");
        
        // To set proxy uncomment the below lines
        // apiClient.setProxyHostName("proxy.address@example.com");
        // apiClient.setProxyPortNumber(0000);

        CompanyApi apiInstance = new CompanyApi(apiClient);
        
        EditCompanyputPayload body = new EditCompanyputPayload(); // Set all the required parameters. Refer to the model documentation below for further information
        
        String enterpriseId = Arrays.asList("enterpriseId_example").get(0); // 
        
        try {
            EditCompanyputResponse result = apiInstance.puteditCompany(body, enterpriseId);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CompanyApi#puteditCompany");
            e.printStackTrace();
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**EditCompanyputPayload**](EditCompanyputPayload.md)|  |
 **enterpriseId** | **String**|  |


### Return type

[**EditCompanyputResponse**](EditCompanyputResponse.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json





##License
**© Copyright 2018 Visa. All Rights Reserved.**

*NOTICE: The software and accompanying information and documentation (together, the “Software”) remain the property of
and are proprietary to Visa and its suppliers and affiliates. The Software remains protected by intellectual property
rights and may be covered by U.S. and foreign patents or patent applications. The Software is licensed and not sold.*

*By accessing the Software you are agreeing to Visa's terms of use (developer.visa.com/terms) and privacy policy (developer.visa.com/privacy).
In addition, all permissible uses of the Software must be in support of Visa products, programs and services provided
through the Visa Developer Program (VDP) platform only (developer.visa.com). **THE SOFTWARE AND ANY ASSOCIATED
INFORMATION OR DOCUMENTATION IS PROVIDED ON AN “AS IS,” “AS AVAILABLE,” “WITH ALL FAULTS” BASIS WITHOUT WARRANTY OR
CONDITION OF ANY KIND. YOUR USE IS AT YOUR OWN RISK.** All brand names are the property of their respective owners, used for identification purposes only, and do not imply
product endorsement or affiliation with Visa. Any links to third party sites are for your information only and equally
do not constitute a Visa endorsement. Visa has no insight into and control over third party content and code and disclaims
all liability for any such components, including continued availability and functionality. Benefits depend on implementation
details and business factors and coding steps shown are exemplary only and do not reflect all necessary elements for the
described capabilities. Capabilities and features are subject to Visa’s terms and conditions and may require development,
implementation and resources by you based on your business and operational details. Please refer to the specific
API documentation for details on the requirements, eligibility and geographic availability.*

*This Software includes programs, concepts and details under continuing development by Visa. Any Visa features,
functionality, implementation, branding, and schedules may be amended, updated or canceled at Visa’s discretion.
The timing of widespread availability of programs and functionality is also subject to a number of factors outside Visa’s control,
including but not limited to deployment of necessary infrastructure by issuers, acquirers, merchants and mobile device manufacturers.*