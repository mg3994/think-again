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


```
<!-- 🟢 PASTE THE DYNAMIC CONFIGURATION CODE HERE -->
    <div style='display:none;'>
      <b:section id='theme-config-section' name='Theme Configuration' maxwidgets='1' showaddelement='no'>
        <b:widget id='Text99' locked='true' title='AppConfig' type='Text' version='2' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='content'>https://api.antinna.in/v1 || MERCH_123456_ANTINNA</b:widget-setting>
          </b:widget-settings>
          <b:includable id='main'>
            <script type='text/javascript'>
              (function() {
                var rawContent = &quot;<data:content/>&quot;;
                var configParts = rawContent.split(&quot; || &quot;);
                
                window.antinnaConfig = {
                  apiUrl: configParts[0] ? configParts[0].trim() : '',
                  merchantId: configParts[1] ? configParts[1].trim() : ''
                };

                console.group(&quot;🚀 Dynamic Blogger Config Loaded From Layout&quot;);
                console.log(&quot;API Base URL:&quot;, window.antinnaConfig.apiUrl);
                console.log(&quot;Merchant ID :&quot;, window.antinnaConfig.merchantId);
                console.groupEnd();
              })();
            </script>
          </b:includable>
        </b:widget>
      </b:section>
    </div>
    <!-- 🛑 END OF DYNAMIC CONFIGURATION CODE -->
```
