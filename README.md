# think-again

Idea 1
```
**
      <!-- Start -->
<!-- Setup custom data tags via b:with and forward them to JavaScript -->
    <b:with value='"https://api.antinna.in/v1"' var='apiBaseUrl'>
    <b:with value='"MERCH_123456_ANTINNA"' var='merchantId'>
        <script type='text/javascript'>
            window.antinnaConfig = {
                apiUrl: '<data:apiBaseUrl/>',
                merchantId: '<data:merchantId/>'
            };
            console.group("🚀 Blogger Theme Configuration Loaded");
            console.log("API Base URL:", window.antinnaConfig.apiUrl);
            console.log("Merchant ID :", window.antinnaConfig.merchantId);
            console.groupEnd();
        </script>
    </b:with>
    </b:with>

    <!-- END  -->
**
```
