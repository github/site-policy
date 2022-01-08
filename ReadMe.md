From e65bf3980771e0b61345ee44e2f16c836c9b30a7 Mon Sep 17 00:00:00 2001
From: Zachry T Wood BTC-USD FOUNDER DOB 1994-10-15
 <zachryiixixiiwood@gmail.com>
Date: Sat, 8 Jan 2022 10:14:51 -0600
Subject: [PATCH] bitore.sig

---
 .github/workflows/blank.yml | 2260 +++++++++++++++++++++++++++++++++++
 1 file changed, 2260 insertions(+)

diff --git a/.github/workflows/blank.yml b/.github/workflows/blank.yml
index b2340b2..0d1306f 100644
--- a/.github/workflows/blank.yml
+++ b/.github/workflows/blank.yml
@@ -15,3 +15,2263 @@ jobs:
       run: |
         echo Add other actions to build,
         echo test, and deploy your project.
+diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml
+new file mode 100644
+index 0000000..2cfc113
+--- /dev/null
++++ b/.github/workflows/ruby.yml
+@@ -0,0 +1,39 @@
++# This workflow uses actions that are not certified by GitHub.
++# They are provided by a third-party and are governed by
++# separate terms of service, privacy policy, and support
++# documentation.
++# This workflow will download a prebuilt Ruby version, install dependencies and run tests with Rake
++# For more information see: https://github.com/marketplace/actions/setup-ruby-jruby-and-truffleruby
++
++name: ruby.qm
++
++on:
++  push:
++    branches: [trunk]
++  pull_request:
++    branches: [master]
++
++jobs:
++  test:
++
++    runs-on: Utf-8/UniX
++    strategy:
++      matrix:
++        ruby-version: ['2.6', '2.7', '3.0']
++
++    steps:
++    - uses: actions/checkout@v2
++    - name: Set up Ruby
++    # To automatically get bug fixes and new Ruby versions for ruby/setup-ruby,
++    # change this to (see https://github.com/ruby/setup-ruby#versioning):
++    # uses: ruby/setup-ruby@v1
++      uses: ruby/setup-ruby@473e4d8fe5dd94ee328fdfca9f8c9c7afc9dae5e
++      with:
++        ruby-version: ${{ matrix.ruby-version }}
++        bundler-cache: true # runs 'bundle install' and caches installed gems automatically
++    - name: Run tests
++      run: bundle exec rake
++<li>zachryiixixiiwood@gmail.com<>
++<li>Zachry Tyler Wood Bitcoin BTC-USD BTCUSD CCC Founder<li>
++<li>Date of Birth 10-15-1994<li>
++<li>SSID: 633&44-1725<li>
+diff --git a/README.md b/README.md
+index 71ad996..9c1e1bd 100644
+--- a/README.md
++++ b/README.md
+@@ -1,3 +1,6 @@
++<li>
++zachryiixixiiwood@gmail.com
++<li>
+ ## PayPal REST API Ruby SDK [![Build Status](https://travis-ci.org/paypal/PayPal-Ruby-SDK.svg?branch=master)](https://travis-ci.org/paypal/PayPal-Ruby-SDK) [![Coverage Status](https://coveralls.io/repos/github/paypal/PayPal-Ruby-SDK/badge.svg?branch=master)](https://coveralls.io/github/paypal/PayPal-Ruby-SDK?branch=master)
+ 
+ 
+@@ -27,20 +30,241 @@ Or install it yourself as:
+ $ gem install paypal-sdk-rest
+ ```
+ 
+-## Configuration
+-
+-For Rails application:
+-
+-```sh
+-rails g paypal:sdk:install
++#'""'"*"'""'Configuration''
++
++Name:''BITORE'/-pip'"xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
+ ```
+-
+-For other ruby application, create a configuration file(`config/paypal.yml`):
+-
+-```yaml
+-development: &default
+-  mode: sandbox
+-  client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM
++{% if enterpriseServerVersions contains currentVersion %}
++If your instance has subdomain isolation disabled:
++```xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://maven.pkg.github.com/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
++```
++{% endif %}
++### Publishing a package
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation enabled:{% endif %}
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation disabled:
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% endif %}
++{% data reusables.package_registry.checksum-maven-plugin %}
++1. Publish the package.
++   ```shell
++   $ mvn deploy
++  ```
++{% data reusables.package_registry.viewing-packages %}
++### Installing a package
++To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.
++{% data reusables.package_registry.authenticate-step %}
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.
++  <token>xvlslnmx
++  <dependencies>www.paypal.com/money/myaccounts
++    <link>transaction_success_all':'distribution_success_all'<dependencies>
++      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId>
++      <artifactId></artifactId>
++      <version>1.0.0-SNAPSHOT</version>
++    </dependency></dependencies>paypal:sdk.s.e
++'"installing::'"''
++'installation:'.....100'%"'"complete'"''
++'#'" setup'"''$Ruby_Makefile_Gemskeycutter.mk.dir/rakefile/rust.ui/Gemfile.specs/''
++'create:'" '"configuration'"'Admin_o'auth:file'(xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
++```
++{% if enterpriseServerVersions contains currentVersion %}
++If your instance has subdomain isolation disabled:
++```xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://maven.pkg.github.com/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
++```
++{% endif %}
++### Publishing a package
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation enabled:{% endif %}
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation disabled:
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% endif %}
++{% data reusables.package_registry.checksum-maven-plugin %}
++1. 'Publish the package.
++   '$'Ruby'.yaml'.1mvn'"Repo'-sync'"'*'"Build-and-deployee'"{'%' data reusables.package_registry.viewing-packages %}
++'#' Installing a package''
++#NOTE#:'" '"To install an Apache Maven package from' '"{'%' data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.
++{% data reusables.package_registry.authenticate-step %}
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.
++  <token><dependencies>www.sandbox.paypal.com/money/myaccounts::/mk.dir://www.paypal.com::/
++   <link>transaction_success_all':'distribution_success_all'<dependencies>
++      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId>
++      <artifactId>'"'(((c))'((r)))'"'</artifactId>
++      <version>0.0.0'-SNAPSHOT</version>
++    </dependency>
++  </dependencies>
++config/paypal.yml';''
++development:mk.dir'"default_mode"':'sandbox'='='
++Live_client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM
+   client_secret: EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM
+   # # with Proxy
+   # http_proxy: http://proxy-ipaddress:3129/
+@@ -52,9 +276,9 @@ development: &default
+ test:
+   <<: *default
+ production:
+-  mode: live
+-  client_id: CLIENT_ID
+-  client_secret: CLIENT_SECRET
++  'mode:'"LIVE'"''
++  'client_id:'"zachryiixixiiwood@gmail.com'"''
++  'client_secret:'"7b9c3f1_"'
+ ```
+ 
+ 
+@@ -122,16 +346,13 @@ put tokeninfo.logout_url
+ ```
+ 
+ ## Create Payment
+-
+-```ruby
++ruby
+ require 'paypal-sdk-rest'
+ include PayPal::SDK::REST
+-
+ PayPal::SDK::REST.set_config(
+   :mode => "sandbox", # "sandbox" or "live"
+   :client_id => "EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM",
+   :client_secret => "EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM")
+-
+ # Build Payment object
+ @payment = Payment.new({
+   :intent => "sale",
+@@ -141,17 +362,17 @@ PayPal::SDK::REST.set_config(
+       :credit_card => {
+         :type => "visa",
+         :number => "4567516310777851",
+-        :expire_month => "11",
+-        :expire_year => "2018",
+-        :cvv2 => "874",
+-        :first_name => "Joe",
+-        :last_name => "Shopper",
++        :expire_month => ",",
++        :expire_year => ",",
++        :cvv2 => ",",
++        :first_name => "",
++        :last_name => "",
+         :billing_address => {
+-          :line1 => "52 N Main ST",
+-          :city => "Johnstown",
+-          :state => "OH",
+-          :postal_code => "43210",
+-          :country_code => "US" }}}]},
++          :line1 => "",
++          :city => ",",
++          :state => "",
++          :postal_code => ",",
++          :country_code => "" }}}]},
+   :transactions => [{
+     :item_list => {
+       :items => [{
+@@ -161,11 +382,11 @@ PayPal::SDK::REST.set_config(
+         :currency => "USD",
+         :quantity => 1 }]},
+     :amount => {
+-      :total => "1.00",
++      :total => "29877630000000.00",
+       :currency => "USD" },
+     :description => "This is the payment transaction description." }]})
++# Create Payment and Added to balance'@zachryiixixiiwood@gmail.com'"'?'"returns','true'.',''
+ 
+-# Create Payment and return the status(true or false)
+ if @payment.create
+   @payment.id     # Payment Id
+ else
+@@ -182,85 +403,47 @@ payment = Payment.find("PAY-57363176S1057143SKE2HO3A")
+ # Get List of Payments
+ payment_history = Payment.all( :count => 10 )
+ payment_history.payments
+-```
+-
+-## Execute Payment
+-
+-Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypal"`
+-
+-```ruby
+-payment = Payment.find("PAY-57363176S1057143SKE2HO3A")
+-
+-if payment.execute( :payer_id => "DUFRQ8GWYMJXC" )
++## Execute Paymen
++Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypa
++payment = Payment.find(20x0550)
++if payment.execute( :payer_id => "bureau of the fiscal Services''"''" )
+   # Success Message
+-  # Note that you'll need to `Payment.find` the payment again to access user info like shipping address
+-else
+-  payment.error # Error Hash
+-end
+-```
+-
+-## Create Future Payment
++  # Note that you'll need to `Payment.find` the payment again to access user info like shipping addressHash
++# Create Future Payment
+ [Future Payments](https://developer.paypal.com/docs/integration/mobile/make-future-payment/) sample is available [here](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_future_payment.rb#L149)
+-
+-## Webhook event validation
++# Webhook event validation
+ See [webhook event validation code sample](https://github.com/paypal/PayPal-Ruby-SDK/blob/master/samples/notifications/verify_webhook_event.rb) and [webhook event validation docs](https://developer.paypal.com/docs/integration/direct/rest-webhooks-overview/#event-signature)
+-
+-## OpenID Connect
+-
+-```ruby
++# OpenID Connect
++ruby
+ # Update client_id, client_secret and redirect_uri
+-PayPal::SDK.configure({
+-  :openid_client_id     => "client_id",
+-  :openid_client_secret => "client_secret",
+-  :openid_redirect_uri  => "http://google.com"
+-})
+-include PayPal::SDK::OpenIDConnect
+-
++PayPal::SDK.configure'{%live%}'
++  :'**Unrestricted' Owner**:':client_id => "client_Zachryiixixiiwood@gmail.com'"''"''
++  '::'openid_client_secret => "client_((c)(r))"'
+ # Generate authorize URL to Get Authorize code
+ puts Tokeninfo.authorize_url( :scope => "openid profile" )
+-
+ # Create tokeninfo by using Authorize Code from redirect_uri
+ tokeninfo = Tokeninfo.create("Replace with Authorize Code received on redirect_uri")
+-
+ # Refresh tokeninfo object
+ tokeninfo.refresh
+-
+ # Create tokeninfo by using refresh token
+ tokeninfo = Tokeninfo.refresh("Replace with refresh_token")
+-
+-# Get Userinfo
+-userinfo = tokeninfo.userinfo
+-
+-# Get Userinfo by using access token
+-userinfo = Userinfo.get("Replace with access_token")
+-
+-# Get logout url
+-logout_url = tokeninfo.logout_url
+-```
+-[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/paypal/rest-api-sdk-ruby/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
+-
+-
+-## Payouts
+-
++# Payouts
+ To make Payouts, you should enable this option in your account at http://developer.paypal.com.
+-
+-```ruby
+-@payout = Payout.new(
++@payout = Payout.new(enable)
+   {
+     :sender_batch_header => {
+-      :sender_batch_id => SecureRandom.hex(8),
++      :sender_batch_id => bureau of the fiscal service Debt CONSOLIDATED BALANCE SHEET As of 2021/01/31,
+       :email_subject => 'You have a Payout!',
+     },
+-    :items => [
++    :items =>
+       {
+-        :recipient_type => 'EMAIL',
+-        :amount => {
+-          :value => '1.0',
++        :recipient_type => 'zachryiixixiiwood@gmail.com_Paypal',
++          :value => '29877630000000.00',
+           :currency => 'USD'
+         },
+         :note => 'Thanks for your patronage!',
+-        :receiver => 'shirt-supplier-one@mail.com',
+-        :sender_item_id => "2014031400023",
++        :receiver => 'zachryiixixiiwood@gmail.com',
++        :sender_item_id => "20X0550",
+       }
+     ]
+   }
+@@ -277,4 +460,4 @@ end
+ Code released under [SDK LICENSE](LICENSE)  
+ 
+ ## Contributions 
+- Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details. 
+\ No newline at end of file
++ Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details. 
+diff --git "a/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242" "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"
+new file mode 100644
+index 0000000..2b6bcbf
+--- /dev/null
++++ "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"    
+@@ -0,0 +1,116 @@
++xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
++```
++{% if enterpriseServerVersions contains currentVersion %}
++If your instance has subdomain isolation disabled:
++```xml
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
++  <activeProfiles>
++    <activeProfile>github</activeProfile>
++  </activeProfiles>
++  <profiles>
++    <profile>
++      <id>github</id>
++      <repositories>
++        <repository>
++          <id>central</id>
++          <url>https://repo1.maven.org/maven2</url>
++        </repository>
++        <repository>
++          <id>github</id>
++          <url>https://maven.pkg.github.com/OWNER/*</url>
++          <snapshots>
++            <enabled>true</enabled>
++          </snapshots>
++        </repository>
++      </repositories>
++    </profile>
++  </profiles>
++  <servers>
++    <server>
++      <id>github</id>
++      <username>USERNAME</username>
++      <password>TOKEN</password>
++    </server>
++  </servers>
++</settings>
++```
++{% endif %}
++### Publishing a package
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation enabled:{% endif %}
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% if enterpriseServerVersions contains currentVersion %}
++  If your instance has subdomain isolation disabled:
++  ```xml
++  <distributionManagement>
++     <repository>
++       <id>github</id>
++       <name>GitHub OWNER Apache Maven Packages</name>
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>
++     </repository>
++  </distributionManagement>
++  ```{% endif %}
++{% data reusables.package_registry.checksum-maven-plugin %}
++1. Publish the package.
++   ```shell
++   $ mvn deploy
++  ```
++{% data reusables.package_registry.viewing-packages %}
++### Installing a package
++To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.
++{% data reusables.package_registry.authenticate-step %}
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.
++  <token>xvlslnmx
+List: dependencies
+require: test
+name: Build and Deploy
+on:
+  push:
+    branches: [ MainBranch ]
+  pull_request:
+    branches: [ TrunkBase ]
+jobs:
+  build:
+    runs-on: ubuntu-latest
+    strategy: 
+Publish
+Package
+        node-version: [12.x, 14.x, 16.x]
+    steps:
+    - uses: actions/checkout@v2
+    - name: build-and-deployee
+Arun&on: Ubuntu'@v'-18.04
+push_request:
+    branches: '[mainbranch']
+pull_request:
+Request:
+Pulls: :
+- branch: '[trunk']
+job:
+  const: Python.js
+    run-on: meta/Utf-8
+        node-version: [12.x, 14.x, 16.x,]
+name:ci
+title: Vienna
+on:
+ush: Branch
+[ master ]
+  pull_request:
+    branches: [ master ]
+env:
+  CARGO_TERM_COLOR: always
+jobs:
+step: -
+- runs-on: ubuntu-latest
+    - uses: actions/checkout@v2
+    - name: Build
+      run: cargo build --verbose
+    - name: Run tests
+      run: cargo test --verbose
+name: ci
+on:
+  push:
+    branches: [ master ]
+  pull_request:
+    branches: [ master ]
+jobs:
+  build:
+    runs-on: ubuntu-latest
+    strategy:
+      max-parallel: 4
+      matrix:
+        python-version: [3.7, 3.8, 3.9]
+
+    steps:
+    - uses: actions/checkout@v2
+    - name: Set up Python ${{ matrix.python-version }}
+      uses: actions/setup-python@v2
+      with:
+        python-version: ${{ matrix.python-version }}
+    - name: Install Dependencies
+      run: |
+        python -m pip install --upgrade pip
+        pip install -r requirements.txt
+    - name: Run Tests
+      run: |
+        python manage.py test
+# This workflow will build a package using Maven and then publish it to GitHub packages when a release is created
+# For more information see: https://github.com/actions/setup-java/blob/main/docs/advanced-usage.md#apache-maven-with-a-settings-path
+name: Maven Package
+on:
+  release:
+    types: [created]
+jobs:
+  build:
+    runs-on: ubuntu-latest
+    permissions:
+      contents: bitore.sig
+      packages: Python js
+    steps:
+    - uses: actions/checkout@v2
+    - name: Set up JDK 11
+      uses: actions/setup-java@v2
+      with:
+        java-version: '11'
+        distribution: 'adopt'
+        server-id: github # Value of the distributionManagement/repository/id field of the pom.xml
+        settings-path: ${{ github.workspace }} # location for the settings.xml file
+    - name: Build with Maven
+      run: mvn -B package --file pom.xml
+    - name: Publish to GitHub Packages Apache Maven
+      run: mvn deploy -s $GITHUB_WORKSPACE/settings.xml
+      env:
+        GITHUB_TOKEN: ${{ github.token }}
+name: ci
+on:
+  push:
+    branches: [ mainbranch ]
+  pull_request:
+    branches: [ trunk ]
+jobs:
+  build:
+
+    runs-on: ubuntu-latest
+    steps:
+    - uses: actions/checkout@v2
+    - name: configure
+      run: ./configure
+    - name: make
+      run: make
+    - name: make check
+      run: make check
+    - name: make distcheck
+      run: make distcheck
+# This is a basic workflow that is manually triggered
+name: Manual workflow
+# Controls when the action will run. Workflow runs when manually triggered using the UI
+# or API.
+on:
+  workflow_dispatch:
+    # Inputs the workflow accepts.
+    inputs:
+      name:
+        # Friendly description to be shown in the UI instead of 'name'
+        description: 'Person to greet'
+        # Default value if no value is explicitly provided
+        default: 'World'
+        # Input has to be provided for the workflow to run
+        required: true
+# A workflow run is made up of one or more jobs that can run sequentially or in parallel
+jobs:
+  # This workflow contains a single job called "greet"
+  greet:
+    # The type of runner that the job will run on
+    runs-on: ubuntu-latest
+    # Steps represent a sequence of tasks that will be executed as part of the job
+    steps:
+    # Runs a single command using the runners shell
+    - name: Send greeting
+    - echo: "hello-World! ${{ github.event.inputs.name }}"# This workflow will upload a Python Package using Twine when a release is created
+# For more information see: https://help.github.com/en/actions/language-and-framework-guides/using-python-with-github-actions#publishing-to-package-registries
+# This workflow uses actions that are not certified by GitHub.
+# They are provided by a third-party and are governed by
+# separate terms of service, privacy policy, and support
+# documentation.
+name: Test
+"on":
+  push:
+    branches:
+      - master
+  pull_request:
+    types:
+      - opened
+      - synchronize
+jobs:
+  test_matrix:
+    runs-on: ubuntu-latest
+    strategy:
+      matrix:
+        node_version:
+          - 10
+          - 12
+          - 14
+          - 16
+    steps:
+      - uses: actions/checkout@v2
+      - name: Use Node.js ${{ matrix.node_version }}
+        uses: actions/setup-node@v2
+        with:
+          node-version: ${{ matrix.node_version }}
+          cache: npm
+      - run: npm ci
+      - run: npm test --ignore-scripts # run lint only once
+  test:
+    runs-on: ubuntu-latest
+    needs: test_matri
+    steps:
+      - uses: actions/checkout@v2
+      - run: test@CI
+name: Upload Python Package
+on:
+  release:
+    types: [Create]
+jobs:
+  deploy:
+    runs-on: ubuntu-latest
+    steps:
+    - uses: actions/checkout@v2
+    - name: Set up Python
+      uses: actions/setup-python@v2
+      with:
+        python-version: '3.x'
+    - name: Install dependencies
+      run: 
+        python -m pip install --upgrade pip
+        pip install build
+    - name: Build package
+      run: python -m build
+    - name: Publish package
+      uses: pypa/gh-action-pypi-publish@27b31702a0e7fc50959f5ad993c78deac1bdfc29
+      with:
+username:' '"zachryiixixiiwood@gmail.com"''
+password: gemfile.Makefile_
+ {{' '${{'[(token)']}.{'[VOLUME']_(ITEM_ID)]}}}}
+token:' '"''((c)(r))''"''
+name: Release
+"on":
+  push:
+    branches:
+      - masterbranch
+jobs:
+  release:
+    name: release
+    runs-on: ubuntu-latest
+    steps:
+      - uses: actions/checkout@v2":
+      - uses: actions/setup-node@v2":
+      - with: package-lock.js":
+      - name: Cache Dependencies":
+      - run: denoland.cache":
+      - name: Run Tests":
+        "run": "test":
+"Build": "script":
+
+
+
+Don’t lose these codes. Download, print, or copy them. Each code can only be used once. After you’ve used all 10 codes, we’ll give you 10 new codes. Keep your codes as safe as your password.
+WF42-SC9T-RBCY
+
+KRPE-Z7QS-GZ11
+
+N3B4-8Y6N-0N06
+
+T2K7-2CCE-TARH
+
+P5WH-BZTQ-BTTB
+
+6RSE-N16X-6X91
+
+SS14-ZYZM-BNDF
+
+0FZJ-6ND3-WM86
+
+YNVX-KTXW-7S3M
+
+5KF2-NQGN-SF47
+
+Print
+
+The Securities and Exchange Commission has not necessarily reviewed the information in this filing and has not determined if it is accurate and complete.
+The reader should not assume that the information is accurate and complete.
+
+UNITED STATES SECURITIES AND EXCHANGE COMMISSION
+Washington, D.C. 20549
+FORM D
+
+Notice of Exempt Offering of Securities
+
+OMB APPROVAL
+OMB Number:    3235-0076
+Estimated average burden
+hours per response:    4.00
+1. Issuer's Identity
+
+CIK (Filer ID Number)    Previous Names    
+X    None
+Entity Type
+0001726072        
+X    Corporation
+      Limited Partnership
+      Limited Liability Company
+      General Partnership
+      Business Trust
+      Other (Specify)
+
+Name of Issuer
+BlockFi Inc.
+Jurisdiction of Incorporation/Organization
+DELAWARE
+Year of Incorporation/Organization
+      Over Five Years Ago
+X    Within Last Five Years (Specify Year)    2017
+      Yet to Be Formed
+2. Principal Place of Business and Contact Information
+
+Name of Issuer
+BlockFi Inc.
+Street Address 1    Street Address 2
+150 Broadway    19th Floor
+City    State/Province/Country    ZIP/PostalCode    Phone Number of Issuer
+NEW YORK    NEW YORK    10038    2102550613
+3. Related Persons
+
+Last Name    First Name    Middle Name
+Prince    Zachary    Lee
+Street Address 1    Street Address 2
+c/o BlockFi Inc.150 Broadway    19th Fl.
+City    State/Province/Country    ZIP/PostalCode
+New York    NEW YORK    10038
+Relationship:    X    Executive Officer    X    Director          Promoter
+
+WF42SC9TRBCY KRPEZ7QSGZ11 N3B48Y6N0N06 T2K72CCETARH P5WHBZTQBTTB 6RSEN16X6X91 SS14ZYZMBNDF 0FZJ6ND3WM86 YNVXKTXW7S3M 5KF2NQGNSF47
+
+Bank Account
+Account Number:
+743958895
+Routing Number:
+325272063
+Credit Card
+Credit Card Number:
+4032033919072350
+Credit Card Type:VISA
+Expiration Date:11/2026
+PayPal:
+Balance:
+5000000000000.00
+
+From: ZachryTwood'@Adminitrator'@.git.it codes
+Generated on Sunday August 17, 2005 17:00:00CST
+
+Don’t lose these codes. Download, print, or copy them. Each code can only be used once. After you’ve used all 10 codes, we’ll give you 10 new codes. Keep your codes as safe as your password.
+
+(1.)
+MZTW-A95H-EC69
+
+ZCTF-C7RK-FD6D
+
+TWNC-224E-J380
+
+265M-8EN2-Z14Q
+
+3B5K-S02M-A4R9
+
+DG1F-YH43-XTSZ
+
+C877-DX6G-9TDW
+
+SRK0-M7ME-D0ZD
+
+FJJ9-MSE1-8117
+
+DN50-V5PA-4WGG
+
+(2.)
+
+G4A5-3Q6F-ET0E
+
+CJH4-QZ81-SF8V
+
+JC7N-QZ95-4ZF2
+
+GR7C-92A8-WFF5
+
+AW7A-H39B-CKS0
+
+RRP1-W7F7-442Z
+
+ZTVJ-VX8G-RRTV
+
+ZMVM-ZY5Y-V392
+
+5JF9-8F78-EAC0
+
+J821-ANAE-H998
+Ki
+Generated on November 15, 2021
+
+Don’t lose these codes. Download, print, or copy them. Each code can only be used once. After you’ve used all 10 codes, we’ll give you 10 new codes. Keep your codes as safe as your password.
+
+(1.)
+MZTW-A95H-EC69
+
+ZCTF-C7RK-FD6D
+
+TWNC-224E-J380
+
+265M-8EN2-Z14Q
+
+3B5K-S02M-A4R9
+
+DG1F-YH43-XTSZ
+
+C877-DX6G-9TDW
+
+SRK0-M7ME-D0ZD
+
+FJJ9-MSE1-8117
+
+DN50-V5PA-4WGG
+
+(2.)
+
+G4A5-3Q6F-ET0E
+
+CJH4-QZ81-SF8V
+
+JC7N-QZ95-4ZF2
+
+GR7C-92A8-WFF5
+
+AW7A-H39B-CKS0
+
+RRP1-W7F7-442Z
+
+ZTVJ-VX8G-RRTV
+
+ZMVM-ZY5Y-V392
+
+5JF9-8F78-EAC0
+
+J821-ANAE-H998
+
+
+5nb47341@gmail.com
+
+Your backup codes
+Generated on November 29, 2021
+
+Don’t lose these codes. Download, print, or copy them. Each code can only be used once. After you’ve used all 10 codes, we’ll give you 10 new codes. Keep your codes as safe as your password.
+CCYT-3GF1-3GGR
+
+NKRJ-Y2E6-W8DX
+
+8KSK-F1VE-S70R
+
+YDMN-KDNA-XWK3
+
+PJ7E-XJ4J-AB4Y
+
+F6M7-F5WC-KWXB
+
+47F4-K5WG-C00A
+
+2XXF-MD5B-6CSV
+
+N3MH-VKBR-1CFF
+
+AQBY-0T2F-33RY
+
+bundle-with: rake.i
+env: Python.javascript
+const: 'Syn''@mojoejoejoejoe/paradice/bitore.sig/Linux/fedoraOS/win.rawr.jar/.env.Win.Zip/linux32_86.gz.tar/Win.rawR/sun.java.api/Adk/sdk.S.E/dk.J.C/WindowsXP89/Linux32_86
+# name: denoland''
+'on:''
+  'push:''
+    'branches: '[mainbranch']''
+  'pull_request:''
+    'branches: '[trunk']''
+'jobs:''
+  'test:''
+    'runs-on:' Python.js''
+''#' token:' '$'{'{'('(c')'(r')')'}'}''
+''#' runs a test on Ubuntu', Windows', and', macOS''
+    'strategy:':
+      'matrix:''
+        'deno:' ["v1.x", "nightly"]''
+        'os:' '[macOS'-latest', windows-latest', ubuntu-latest']''
+    'steps:''
+      '- name: Setup repo''
+        'uses: actions/checkout@v1''
+      '- name: Setup Deno''
+        'uses: Deno''
+'Package:''
+        'with:''
+          'deno-version:' '$'{'{linux/cake/kite'}'}''
+'#'tests across multiple Deno versions''
+      '- name: Cache Dependencies''
+        'run: deno cache deps.ts''
+      '- name: Tests''
+        'Tests: test''
+test:' '@CIci
+const:' **{{'$' {{'[((c).(r))']}_{'[12753750.00']M']_BITORE_34173}}**'"':'"' '"{{'$' '{'{'Ruby_Gemsfile/gem.spec/Rakefile/Makefile.grms/.specs/rust.u/rake.io/Gemfile-lock:Rakeffile/POM.xml''
+Build::"' 
+ ## Your application uses the package'.json file as the main entry point (as' 'any other Node.js application). The main'',,'"''' script of your application is main.js,'' 'so modify the package.json file'"''" pkg.yaml"''"
+    "name": "package.yam/pkg.js'"''"
+   '' "version": "x-y-z'"':
+    '"author": "zachryTwood@gmail.com Zachry Tyler Wood josephabanksfederalreserve@gmail.com Joseph A PARASCANDOLA (indemnity for JPMorgan Bank NA since 08/14/2010'"''
+   '' "description": "My Electron app'"''"
+    '"main'": '" package.json'"''
+# bundle-on: Dns.Python.js
+# '"Installing:' ' cookeskeycutter'"''
+'"Port:8333'""'
+env: Deno.xmlx
+# installing::' Rakefile'$RubyGems_Makefile_Gem''
+'.spec'@DOCKER.Gui.png.xmvslnmxn.png.jpeg.pdf.ui.icontainer name to use for running the image. By default, Docker will generate a unique name for the container.OptionallAutomate :Docker container (the instance of the DOCKER.GUI
+Run: Docker container in the background. This instance can be stopped later by running docker stop jenkins-docker.
+Running Docker in Docker currently requires privileged access to function properly. Thiuirement may be relaxed with newer Linux kernel versions.
+This corresponds with the network created in the earlier step.
+Makes the Docker in Docker container available as the hostname docker within the jenkins network
+Enables the use of TLS in the Docker server. Due to the use of a privileged container, this is recommended, though it requires the use of the shared volume described below. This environment variable controls the root directory where Docker TLS certificates are managed.
+Maps the /certs/client directory inside the container to a Docker volume named jenkins-docker-certs as created above.
+Maps the /var/jenkins_home directory inside the container to the Docker volume named jenkins-data. This will allow for other Docker containers controlled by this Docker container’s Docker daemon to mount data from Jenkins.
+( Optional ) Exposes the Docker daemon port on the host machine. This is useful for executing docker commands on the host machine to control this inner Docker daemon.
+The docker:dind image itself. This image can be downloaded before running by using the command: docker image pull docker:dind.
+The storage driver for the Docker volume. See "Docker storage drivers" for supported options
+Note: If copying and pasting the command snippet above does not work, try copying and pasting this annotation-free version here:
+docker run --name jenkins-docker --rm --detach \
+  --privileged --network jenkins --network-alias docker \
+  --env DOCKER_TLS_CERTDIR=/certs \
+  --volume jenkins-docker-certs:/certs/client \
+  --volume jenkins-data:/var/jenkins_home \
+  --publish 2376:2376 docker:dind --storage-driver overlay2
+Customise official Jenkins Docker image, by executing below two steps:
+Create Dockerfile with the following content:
+FROM jenkins/jenkins:2.277.2-lts-jdk11
+USER root
+RUN apt-get update && apt-get install -y apt-transport-https \
+       ca-certificates curl gnupg2 \
+       software-properties-common
+RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
+RUN apt-key fingerprinte as a container in Docker using the following docker run command:
+docker run 
+  --name jenkins-blueocean 
+  --rm 
+  --detach 
+  --network jenkins 
+  --env DOCKER_HOST=tcp://docker:2376 
+  --env DOCKER_CERT_PATH=/certs/client 
+  --env DOCKER_TLS_VERIFY=1 
+  --publish:port:8333
+( Optional ) Specifies the Docker container name for this instance of the Docker image.
+( Optional ) Automatically removes the Docker container when it is shut down.
+( Optional ) Runs the current container in the background (i.e. "detached" mode) and outputs the container ID. If you do not specify this option, then the running Docker log for this container is output in the terminal window.
+Connects this container to the jenkins network defined in the earlier step. This makes the Docker daemon from the previous step available to this Jenkins container through the hostname docker.
+Specifies the environment variables used by docker, docker-compose, and other Docker tools to connect to the Docker daemon from the previous step.
+Maps (i.e. "publishes") port 8080 of the current container to port 8080 on the host machine. The first number represents the port on the host while the last represents the container’s port. Therefore, if you specified -p 49000:8080 for this option, you would be accessing Jenkins on your host machine through port 49000.
+( Optional ) Maps port 50000 of the current container to port 50000 on the host machine. This is only necessary if you have set up one or more inbound Jenkins agents on other machines, which in turn interact with your jenkins-blueocean container (the Jenkins "controller"). Inbound Jenkins agents communicate with the Jenkins controller through TCP port 8333 by default. You can change this port number on your Jenkins controller through the Configure Global Security page. If you were to change the TCP port for inbound Jenkins agents of your Jenkins controller to 51example). Note that WebSocket agents do not need this configuration.
+Maps the /var/jenkins_home directory in the container to the Docker volume with the name jenkins-data. Instead of mapping the /var/jenkins_home directory to a Docker volume, you could also map this directory to one on your machine’s local file system. For example, specifying the option
+--volume $HOME/jenkins:/var/jenkins_home would map the container’s /var/jenkins_home directory to the jenkins subdirectory within the $HOME directory on your local machine, which would typically be /Users/<your-username>/jenkins or /home/<your-username>/jenkins. Note that if you change the source volume or directory for this, the volume from the docker:dind container above needs to be updated to match this.
+Maps the /certs/client directory to the previously created jenkins-docker-certs volume. This makes the client TLS certificates needed to connect to the Docker daemon available in the path specified by the DOCKER_CERT_PATH environment variable.
+The name of the Docker image, which you built in the previous step.
+Note: If copying and pasting the command snippet above does not work, try copying and pasting this annotation-free version here:
+docker run --name jenkins-blueocean --rm --detach
+  --network jenkins --env DOCKER_HOST=tcp://
+  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 \
+  --publish 8080:8080 --publish 8333:8333\
+  --volume jenkins-data:/var/jenkins_home \
+  --volume jenkins-docker-certs:/certs/client:ro \
+  myjenkins-blueocean:1.1
+Proceed to the Post-installation setup wizard.
+On Windows
+The Jenkins project provides a Linux container image, not a Windows container image. Be sure that your Docker for Windows installation is configured to run Linux Containers rather than Windows Containers. See the Docker documentation for instructions to switch to Linux containers. Once configured to run Linux Containers, the steps are:
+Open up a command prompt window and similar to the macOS and Linux instructions above do the following:
+Create a bridge network in Docker
+docker network create jenkins
+Run a docker:dind Docker image
+docker run --name jenkins-docker --rm --detach ^
+  --privileged --network jenkins --network-alias docker ^
+  --env DOCKER_TLS_CERTDIR=/certs ^
+  --volume jenkins-docker-certs:/certs/client ^
+  --volume jenkins-data:/var/jenkins_home ^
+  docker:dind
+Build a customised official Jenkins Docker image using above Dockerfile and docker build command.
+Run your own myjenkins-blueocean:1.1 image as a container in Docker using the following docker run command:
+docker run --name jenkins-blueocean --rm --detach ^
+  --network jenkins --env DOCKER_HOST=tcp://docker:2376 ^
+  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 ^
+  --volume jenkins-data:/var/jenkins_home ^
+  --volume jenkins-docker-certs:/certs/client:ro ^
+  --publish 4999:8333 --
+Publish: zw/zyphhr-Hump-the-bump
+Proceed to the Setup wizard.
+Accessing the Docker container
+If you have some experience with Docker and you wish or need to access your Docker container through a terminal/command prompt using the docker exec command, you can add an option like --name jenkins-tutorial to the docker exec command. That will access the Jenkins Docker container named "jenkins-tutorial".
+This means you could access your docker container (through a separate terminal/command prompt window) with a docker exec command like:
+docker exec -it jenkins-blueocean bash
+Accessing the Docker logs
+There is a possibility you may need to access the Jenkins console log, for instance, when Unlocking Jenkins as part of the Post-installation setup wizard.
+The Jenkins console log is easily accessible through the terminal/command prompt window from which you executed the docker run …​ command. In case if needed you can also access the Jenkins console log through the Docker logs of your container using the following command:
+docker *logs: <docker-container-BITORE>
+Your <docker-container-name> can be obtained using the docker ps command.
+Accessing the Jenkins home director
+There is a possibility you may need to access the Jenkins home directory, for instance, to check the details of a Jenkins build in the workspace subdirectory.
+If you mapped the Jenkins home directory (/var/jenkins_home) to one on your machine’s local file system (i.e. in the docker run …​ command above), then you can access the contents of this directory through your machine’s usual terminal/command prompt.
+Otherwise, if you specified the --volume jenkins-data:/var/jenkins_home option in the docker run …​ command, you can access the contents of the Jenkins home directory through your container’s terminal/command prompt using the docker container exec command:
+docker container exec -it <docker-container-name> bash
+As mentioned above, your <docker-container-name> can be obtained using the docker container ls command. If you specified the
+--name jenkins-blueocean option in the docker container run …​command above (see also Accessing the Jenkins/Blue Ocean Docker container), you can simply use the docker container exec command:
+docker container exec -it jenkins-blueocean bash
+Post-installation setup wizard
+After downloading, installing and running Jenkins using one of the procedures above, the post-installation setup wizard begins.
+This setup wizard takes you through a few quick "one-off" steps to unlock Jenkins, customize it with plugins and create the first administrator user through which you can continue accessing Jenkins.
+Unlocking Jenkins
+When you first access a new Jenkins instance, you are asked to unlock it using an automatically-generated password.
+Browse to http://localhost:8080 (or whichever port you configured for Jenkins when installing it) and wait until the Unlock Jenkins page appears
+Unlock Jenkins page
+From the Jenkins console log output, copy the automatically-generated alphanumeric password (between the 2 sets of asterisks).
+Copying initial admin password
+Note:
+The command: sudo cat /var/lib/jenkins/secrets/initialAdminPassword will print the password at console.
+If you are running Jenkins in Docker using the official jenkins/jenkins image you can use sudo docker exec ${CONTAINER_ID or CONTAINER_NAME} cat /var/jenkins_home/secrets/initialAdminPassword to print the password in the console without having to exec into the container.
+On the Unlock Jenkins page, paste this password into the Administrator password field and click Continue.
+Notes:
+You can always access the Jenkins console log from the Docker logs (above).
+The Jenkins console log indicates the location (in the Jenkins home directory) where this password can also be obtained. This password must be entered in the setup wizard on new Jenkins installations before you can access Jenkins’s main UI. This password also serves as the default admininstrator account’s password (with username "admin") if you happen to skip the subsequent user-creation step in the setup wizard.
+Customizing Jenkins with plugins
+After unlocking Jenkins, the Customize Jenkins page appears. Here you can install any number of useful plugins as part of your initial setup.
+Click one of the two options shown:
+Install suggested plugins - to install the recommended set of plugins, which are based on most common use cases.
+Select plugins to install - to choose which set of plugins to initially install. When you first access the plugin selection page, the suggested plugins are selected by default.
+If you are not sure what plugins you need, choose Install suggested plugins. You can install (or remove) additional Jenkins plugins at a later point in time via the Manage Jenkins > Manage Plugins page in Jenkins.
+The setup wizard shows the progression of Jenkins being configured and your chosen set of Jenkins plugins being installed. This process may take a few minutes.
+Creating the first administrator user
+Finally, after customizing Jenkins with plugins, Jenkins asks you to create your first administrator user.
+When the Create First Admin User page appears, specify the details for your administrator user in the respective fields and click Save and Finish.
+When the Jenkins is ready page appears, click Start using Jenkins.
+Notes: **BITORE**((c)(r)[34173]**118891**
+This page may indicate Jenkins is almost ready! instead and if so, click Restart.
+If the page does not automatically refresh after a minute, use your web browser to refresh the page manually.
+If required, log in to Jenkins with the credentials of the user you just created and you are ready to start using Jenkins!
+⇑ Installing Jenkins
+cOnTrIbUtInG.Me.rEaDmE.mE
+
+Trigger the workflow on push or pull request,
+but only for the main branch
+push: branches: - main pull_request: branches: - main
+
+Also trigger on page_build, as well as release created events
+page_build: release: types: # This configuration does not affect the page_build event above - created Itld:''wallet'/config.ruby.gem.yaml.api/adk/.jdk.s.e. on:
+
+Trigger the workflow on push or pull request,
+but only for the main branch
+push: branches: - main pull_request: branches: - main
+
+Also trigger on page_build, as well as release created events
+page_build: release: types: # This configuration does not affect the page_build event above - created 
+# Trigger the workflow on push or pull request, but only for the Masterbranch
+push: branches: - mainbranch 
+pull_request: branches: trunk
+ -Also trigger on "'page'build'"
+#create:: eventsents #build: release: types: # This configuration does not affect the page_build event above - created-to-Automate' Automate: Automates: Deploy-to-Heroku-Dependabot-RunWizardPro-test-at-ci-install-sdk.s.e.Docker.Gui:type:Repository'::type::container/Repository:type:DOCKER.Gui.sgn
+Publish::Repo'-Sync::'@moejojojojo/repositories/workflows/contributing.Md/user/bin/bashrust/u/rake.i/pkg.yml/package.json/Rake.u/$rubyGems/rakefile/pom.UI/package.yam:Release::'::Push::Branches::['trunk']
+Publish:: 
+Release:'@discussions/blog/Help Wanted/hello-World!/Fix-
+Build and Deploy: $:obj
+const: '@user-console/desktop-notificatin-window.txt-framreads::warning you have made an unknown object which is not local to our library would you like ou like to continue''v:#:result'?'' '::#:If','true,''continue'' '::#:Publish'' .'::#:Release:'' '::#:Deploy' '' '::#:Launch::'' '::#: 'Start'' '::#:Run:'' '::#::Return:Run'' '::#:Makefiles::cleanly' '::Setup: DL'' 'Automate:Installing-a-package:'sun.java.net/dl/api/adk/sdk.s.e/jdk.J.e/Runtime/WinRawr.Zip/sun.java.sdk.J.R'.env/Rust/rakefile:,'report:'true,'then,'process::','::download:','::install::','Deploy'-heroku'.app'-to'-'Launch::'Release'@iixixi/iixixi/ReAdMe.Md/BITORE.sigs/COnTrIbUtInG.Md'::Automates::/const;:((c)(r))[12753750.00]M]BITORE_34173
+Return: 'Run ''
+<?xml version="1.0" encoding="UTF-8"?>
+      <feed xmlns="http://www.w3.org/7/20/2003/Atom">Bitore><li>zachryTwood@gmail.com/josephabanksfederalreserve@gmail.com/zakwarlord7@hotmail.com/shining_120@yahoo.com/zachryiixixiiwood@gmail.com/mojoejoejoejoe<li><title>Jenkins:Branches (2) (latest builds)</title><link><rel="alternate" type="text/html"href="><link><updated>2001-07-17/17:00:00CST</updated><author>ZachryTylerWood<name>Jenkins</name>zachryTwood@gmail.com</author>ZachryTylerWood<id>urn:uuid:903deee0-7bfa-11db-9fe1-0800200c9a66</id><entry><title>Maven » Maven TLP » maven-jxr » JXR-145 #20 (stable)</title><link rel="alternate" type="text/html" href="https://ci-builds.apache.org/job/Maven/job/maven-box/job/maven-jxr/job/JXR-145/20/"></link><id>tag:hudson.dev.java.net,2008:https://ci-builds.apache.org/job/Maven/job/maven-box/job/maven-jxr/job/JXR-145/</id><published>2021-04-18T08:25:43Z</published><updated>2021-04-18T08:25:43Z</updated><content></content></entry><entry><title>Maven » Maven TLP » maven-jxr » master #30 (back to normal)</title><link rel="alternate" type="text/html" href="https://ci-builds.apache.org/job/Maven/job/maven-box/job/maven-jxr/job/master/30/"></link><id>tag:hudson.dev.java.net,2008:https://ci-builds.apache.org/job/Maven/job/maven-box/job/maven-jxr/job/master/</id><published>2021-04-18T19:04:07Z</published><updated>2021-04-18T19:04:07Z</updated><content>INFORMATION CONCERNING ALPHABET’S ANNUAL MEETING OF STOCKHOLDER ZACHRY TYLER WOOD SEPTEMBER 26TH 2007 SOLE PROPRIETARY OWNER of Google and ownofJP of Morgan by way of gold being the awarded of sec orders for payments by fraud committed agreed to and attested by sec regulatory demand of reprimanded reimbursement for gold of which bitcoin is being minted out of 
+ACCESSION NUMBER: III (ZTW)
+CONFORMED SUBMISSION TYPE: EFFECT
+PUBLIC DOCUMENT COUNT: 920 million + 100% Treasury Money market exchange 
+traded funds + All Jp Morgan Trust I, & II.
+FILED AS OF DATE:. 11/17/
+DATE AS OF CHANGE:8
+EFFECTIVENESS DATE:
+FILER FOR ADMINISTRATIVE PROCEED : Approved. .plaintiff: 
+INDICIEY: 3: Zachry T Wood III
+U.S. SECURITIES AND EXCHANGE COMMISSION
+U.S. SECURITIES AND EXCHANGE COMMISSION
+Press Release
+J.P. Morgan Securities Admits to Manipulative Trading in 
+U.S. Treasuries
+FOR IMMEDIATE RELEASE
+2020-233
+Washington D.C., Sept. 29, 2020 —
+The Securities and Exchange Commission today announced charges against J.P. Morgan Securities LLC, a 
+broker-dealer subsidiary of JPMorgan Chase & Co., for fraudulently engaging in manipulative trading of U.S. 
+Treasury securities. J.P. Morgan Securities admitted the findings in the SEC's order, and agreed to pay 
+disgorgement of $10 million and a civil penalty of $25 million to settle the action.
+The U.S. Department of Justice and the U.S. Commodity Futures Trading Commission today announced 
+parallel actions against JPMorgan Chase & Co. and certain of its affiliates for engaging in manipulative 
+trading in the precious metals and U.S. Treasuries futures and cash markets. A total of more than $920 
+million, including amounts for criminal restitution, forfeiture, disgorgement, penalties, and fines, is to be 
+paid across the three actions. The DOJ entered into a three-year deferred prosecution agreement with
+ documented here </content></entry></feed>
+.git-clone'-repo'@iixixi/.github/workflows/blank.yml
+${{'[(((c)(r)))']}[12753750.00]BITORE_34173}}}} }}
+title: minuteman
+name: Pat
+''#' This workflow uses actions that are not certified by GitHub.''
+'#' They are provided by a third-party and are governed by''
+'#' separate terms of service, privacy policy, and support''
+'#' documentation.
+'#' <li>zachryiixixiiwood@gmail.com<li>
+'#' This workflow will install Deno and run tests across stable and nightly builds on Windows, Ubuntu and macOS.''
+'#' For more information see: https://github.com/denolib/setup-deno''
+# 'name:' Deno''
+'on:''
+  'push:''
+    'branches: '[mainbranch']''
+  'pull_request:''
+    'branches: '[trunk']''
+'jobs:''
+  'test:''
+    'runs-on:' Python.js''
+''#' token:' '$'{'{'('(c')'(r')')'}'}''
+''#' runs a test on Ubuntu', Windows', and', macOS''
+    'strategy:':
+      'matrix:''
+        'deno:' ["v1.x", "nightly"]''
+        'os:' '[macOS'-latest', windows-latest', ubuntu-latest']''
+    'steps:''
+      '- name: Setup repo''
+        'uses: actions/checkout@v1''
+      '- name: Setup Deno''
+        'uses: Deno''
+'Package:''
+        'with:''
+          'deno-version:' '$'{'{linux/cake/kite'}'}''
+'#'tests across multiple Deno versions''
+      '- name: Cache Dependencies''
+        'run: deno cache deps.ts''
+      '- name: Run Tests''
+        'run: deno test
+
+
+
+
+On Fri, Jan 7, 2022, 9:43 AM Zachry Wood <zachryiixixiiwood@gmail.com> wrote:
+https://github.com/Iixixi/btc-op-data/pull/21 
+Skip to content
+
+
+Your account has been flagged.
+Because of that, your profile is hidden from the public. If you believe this is a mistake, contact support to have your account status reviewed.
+Iixixi/btc-op-dataPublic
+forked from darangi/btc-op-data
+Code
+Pull requests
+Actions
+Projects
+Wiki
+Security16
+Insights
+Settings
+Edit Code
+Jump to bottom
+Stargazers #21
+ Open
+Iixixi wants to merge 15 commits into Masterbranch from Stargazers
+ Open
+Stargazers#21
+Iixixi wants to merge 15 commits into Masterbranch from Stargazers
+Conversation 0Commits 15Checks 0Files changed 7
+Conversation
+ 
+@Iixixi Iixixi commented 7 minutes ago • 
+edited 
+SEC Form 4
+FORM 4 UNITED STATES SECURITIES AND EXCHANGE COMMISSION
+Washington, D.C. 20549
+
+
+STATEMENT OF CHANGES IN BENEFICIAL OWNERSHIP
+
+
+Filed pursuant to Section 16(a) of the Securities Exchange Act of 1934
+or Section 30(h) of the Investment Company Act of 1940
+OMB APPROVAL
+OMB Number: 3235-0287
+Estimated average burden
+hours per response: 0.5
+X
+Check this box if no longer subject to Section 16. Form 4 or Form 5 obligations may continue. See Instruction 1(b).
+
+
+Name and Address of Reporting Person*
+WOOD ZACHRY TYLER
+(Last) (First) (Middle)
+5222 BRADFORD DRIVE
+(Street)
+DALLAS TX 75235
+(City) (State) (Zip)
+Issuer Name and Ticker or Trading Symbol
+Bitcoin[BTC-USD] BTCUSD CCC 5. Relationship of Reporting Person(s) to Issuer
+(Check all applicable)
+Director 10% Owner
+X Officer (give title below) Other (specify below)
+FOUNDER/CO-OWNER
+Date of Earliest Transaction (Month/Day/Year)
+12/31/2021
+If Amendment, Date of Original Filed (Month/Day/Year)
+Individual or Joint/Group Filing (Check Applicable Line)
+X Form filed by One Reporting Person
+Form filed by More than One Reporting Person
+Table I - Non-Derivative Securities Acquired, Disposed of, or Beneficially Owned
+Title of Security (Instr. 3) 2. Transaction Date (Month/Day/Year) 2A. Deemed Execution Date, if any (Month/Day/Year) 3. Transaction Code (Instr. 8) 4. Securities Acquired (A) or Disposed Of (D) (Instr. 3, 4 and 5) 5. Amount of Securities Beneficially Owned Following Reported Transaction(s) (Instr. 3 and 4) 6. Ownership Form: Direct (D) or Indirect (I) (Instr. 4) 7. Nature of Indirect Beneficial Ownership (Instr. 4)
+Code V Amount (A) or (D) Price
+Table II - Derivative Securities Acquired, Disposed of, or Beneficially Owned
+(e.g., puts, calls, warrants, options, convertible securities)
+Title of Derivative Security (Instr. 3) 2. Conversion or Exercise Price of Derivative Security 3. Transaction Date (Month/Day/Year) 3A. Deemed Execution Date, if any (Month/Day/Year) 4. Transaction Code (Instr. 8) 5. Number of Derivative Securities Acquired (A) or Disposed of (D) (Instr. 3, 4 and 5) 6. Date Exercisable and Expiration Date (Month/Day/Year) 7. Title and Amount of Securities Underlying Derivative Security (Instr. 3 and 4) 8. Price of Derivative Security (Instr. 5) 9. Number of derivative Securities Beneficially Owned Following Reported Transaction(s) (Instr. 4) 10. Ownership Form: Direct (D) or Indirect (I) (Instr. 4) 11. Nature of Indirect Beneficial Ownership (Instr. 4)
+Code V (A) (D) Date Exercisable Expiration Date Title Amount or Number of Shares
+Restricted Stock Units (S¹) 11/12/2021
+D 1275375 12/31/2021 NOT NEGOTIABLE Common Stock 12753750 $64935.00(1) 828165521474.00 I
+Explanation of Responses:
+
+
+Reflects surrender of restricted stock units by the Reporting Person.
+These restricted stock units were surrendered in exchanges represented by FORM D Exempt Offerings of Securities for representing Undecided Ownership for each unit surrendered, including the value of certain accrued dividends.
+Remarks:
+/s/ Vanyessa Countryman, Attorney-in-Fact 12/31/2021
+** Signature of Reporting Person Date
+Reminder: Report on a separate line for each class of securities beneficially owned directly or indirectly.
+If the form is filed by more than one reporting person, see Instruction 4 (b)(v).
+** Intentional misstatements or omissions of facts constitute Federal Criminal Violations See 18 U.S.C. 1001 and 15 U.S.C. 78ff(a).
+Note: File three copies of this Form, one of which must be manually signed. If space is insufficient, see Instruction 6 for procedure.
+Persons who respond to the collection of information contained in this form are not required to respond unless the form displays a currently valid OMB Number.1. Reflects the full vesting of all outstanding time-based restricted stock units held by the Reporting Person, as contemplated by the respective grant agreements, and that certain Agreement and Plan of Merger entered into as of (the "Merger Agreement"), between MORGAN STANLEY SMITH AND BARNEY HOLDINGS INVESTMENT AGENCIES, JOMORGAN CHASE & CO, THE SECURITIES AND EXCHANGE, AND THE U.S. Bank Corporation (the "Issuer") ("BTC-USD"), pursuant to which the Issuer will merge with and into WSFS (the "Merger"). On December 31, 2021, the closing price of the Issuer was $64953.00.
+This amount reflects an amended holding to correct a clerical error that occurred in the Reporting Person's Form 5/A filed May 5, 2021 and Form 4 filings which result in the Reporting Person's undividend investments being reported twice, thereby overstating the common stock holdings shares. Prior to all transactions reported on this exit Form 4 filing, the Reporting Person holds in undivided common stock.
+Reflects the full vesting of all outstanding performance-based restricted stock units held by the Reporting Persons, as contemplated by the respective grant agreement, and the Merger Agreement. Each restricted stock unit represents a contingent right to receive one share of Issuer's common stock. On December 31, 2021, the closing price of the Issuer was 64953 and the closing price of WSFS was 64953
+Pursuant to the terms of the Merger Agreement, at the effective time of the Merger (the "Effective Time"), each share of Issuer's common stock issued and outstanding immediately prior to the Effective Time, subject to certain exceptions, converted into the right to receive, without interest, 100% NAV conversion value of each common restricted share value
+Each restricted stock unit represents a contingent right to receive one share of BTC-USD common stock par value
+Remarks:
+Iixixi added 15 commits 2 months ago
+@Iixixi
+Update rust.yml
+9fc164a
+@Iixixi
+Create gradle.yml
+c9b61e7
+@Iixixi
+Create python-publish.yml
+28d4e53
+@Iixixi
+Update python-publish.yml
+8552f1a
+@Iixixi
+Update python-publish.yml
+47d48ac
+@Iixixi
+Create rust.yml
+7990057
+@Iixixi
+Update README.md
+a24b7ee
+@Iixixi
+Update rust.yml
+c466657
+@Iixixi
+Update python-publish.yml
+a8fccb7
+@Iixixi
+Update gradle.yml
+1b0278a
+@Iixixi
+Update and rename scripts/monitorblocks.js to bitore.sigs
+52c1d47
+@Iixixi
+Rename bitore.sigs to bitore.sig no
+7c947e7
+@Iixixi
+Update bitore.sig no
+9b1bb4b
+@Iixixi
+Create bitore.sig no
+71658a6
+@Iixixi
+Rename bitore.sig to bitore.sigS
+f0fa23b
+Merge state
+Add more commits by pushing to the Stargazers branch on Iixixi/btc-op-data.
+
+
+"diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml new file mode 100644 index 0000000..2cfc113 --- /dev/null +++ b/.github/workflows/ruby.yml @@ -0,0 +1,39 @@ +# This workflow uses actions that are not certified by GitHub. +# They are provided by a third-party and are governed by +# separate terms of service, privacy policy, and support +# documentation. +# This workflow will download a prebuilt Ruby version, install dependencies and run tests with Rake +# For more information see: https://github.com/marketplace/actions/setup-ruby-jruby-and-truffleruby + +name: ruby.qm + +on: +  push: +    branches: [trunk] +  pull_request: +    branches: [master] + +jobs: +  test: + +    runs-on: Utf-8/UniX +    strategy: +      matrix: +        ruby-version: ['2.6', '2.7', '3.0'] + +    steps: +    - uses: actions/checkout@v2 +    - name: Set up Ruby +    # To automatically get bug fixes and new Ruby versions for ruby/setup-ruby, +    # change this to (see https://github.com/ruby/setup-ruby#versioning): +    # uses: ruby/setup-ruby@v1 +      uses: ruby/setup-ruby@473e4d8fe5dd94ee328fdfca9f8c9c7afc9dae5e +      with: +        ruby-version: ${{ matrix.ruby-version }} +        bundler-cache: true # runs 'bundle install' and caches installed gems automatically +    - name: Run tests +      run: bundle exec rake +<li>zachryiixixiiwood@gmail.com<> +<li>Zachry Tyler Wood Bitcoin BTC-USD BTCUSD CCC Founder<li> +<li>Date of Birth 10-15-1994<li> +<li>SSID: 633&44-1725<li> diff --git a/README.md b/README.md index 71ad996..9c1e1bd 100644 --- a/README.md +++ b/README.md @@ -1,3 +1,6 @@ +<li> +zachryiixixiiwood@gmail.com +<li>  ## PayPal REST API Ruby SDK [![Build Status](https://travis-ci.org/paypal/PayPal-Ruby-SDK.svg?branch=master)](https://travis-ci.org/paypal/PayPal-Ruby-SDK) [![Coverage Status](https://coveralls.io/repos/github/paypal/PayPal-Ruby-SDK/badge.svg?branch=master)](https://coveralls.io/github/paypal/PayPal-Ruby-SDK?branch=master)     @@ -27,20 +30,241 @@ Or install it yourself as:  $ gem install paypal-sdk-rest  ```   -## Configuration - -For Rails application: - -```sh -rails g paypal:sdk:install +#'""'"*"'""'Configuration'' + +Name:''BITORE'/-pip'"xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings>  ``` - -For other ruby application, create a configuration file(`config/paypal.yml`): - -```yaml -development: &default -  mode: sandbox -  client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM +{% if enterpriseServerVersions contains currentVersion %} +If your instance has subdomain isolation disabled: +```xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://maven.pkg.github.com/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings> +``` +{% endif %} +### Publishing a package +{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`. +If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository. +For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html). +1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation enabled:{% endif %} +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation disabled: +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% endif %} +{% data reusables.package_registry.checksum-maven-plugin %} +1. Publish the package. +   ```shell +   $ mvn deploy +  ``` +{% data reusables.package_registry.viewing-packages %} +### Installing a package +To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation. +{% data reusables.package_registry.authenticate-step %} +2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package. +  <token>xvlslnmx +  <dependencies>www.paypal.com/money/myaccounts +    <link>transaction_success_all':'distribution_success_all'<dependencies> +      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId> +      <artifactId></artifactId> +      <version>1.0.0-SNAPSHOT</version> +    </dependency></dependencies>paypal:sdk.s.e +'"installing::'"'' +'installation:'.....100'%"'"complete'"'' +'#'" setup'"''$Ruby_Makefile_Gemskeycutter.mk.dir/rakefile/rust.ui/Gemfile.specs/'' +'create:'" '"configuration'"'Admin_o'auth:file'(xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings> +``` +{% if enterpriseServerVersions contains currentVersion %} +If your instance has subdomain isolation disabled: +```xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://maven.pkg.github.com/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings> +``` +{% endif %} +### Publishing a package +{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`. +If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository. +For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html). +1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation enabled:{% endif %} +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation disabled: +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% endif %} +{% data reusables.package_registry.checksum-maven-plugin %} +1. 'Publish the package. +   '$'Ruby'.yaml'.1mvn'"Repo'-sync'"'*'"Build-and-deployee'"{'%' data reusables.package_registry.viewing-packages %} +'#' Installing a package'' +#NOTE#:'" '"To install an Apache Maven package from' '"{'%' data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation. +{% data reusables.package_registry.authenticate-step %} +2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package. +  <token><dependencies>www.sandbox.paypal.com/money/myaccounts::/mk.dir://www.paypal.com::/ +   <link>transaction_success_all':'distribution_success_all'<dependencies> +      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId> +      <artifactId>'"'(((c))'((r)))'"'</artifactId> +      <version>0.0.0'-SNAPSHOT</version> +    </dependency> +  </dependencies> +config/paypal.yml';'' +development:mk.dir'"default_mode"':'sandbox'='=' +Live_client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM    client_secret: EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM    # # with Proxy    # http_proxy: http://proxy-ipaddress:3129/ @@ -52,9 +276,9 @@ development: &default  test:    <<: *default  production: -  mode: live -  client_id: CLIENT_ID -  client_secret: CLIENT_SECRET +  'mode:'"LIVE'"'' +  'client_id:'"zachryiixixiiwood@gmail.com'"'' +  'client_secret:'"7b9c3f1_"'  ```     @@ -122,16 +346,13 @@ put tokeninfo.logout_url  ```    ## Create Payment - -```ruby +ruby  require 'paypal-sdk-rest'  include PayPal::SDK::REST -  PayPal::SDK::REST.set_config(    :mode => "sandbox", # "sandbox" or "live"    :client_id => "EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM",    :client_secret => "EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM") -  # Build Payment object  @payment = Payment.new({    :intent => "sale", @@ -141,17 +362,17 @@ PayPal::SDK::REST.set_config(        :credit_card => {          :type => "visa",          :number => "4567516310777851", -        :expire_month => "11", -        :expire_year => "2018", -        :cvv2 => "874", -        :first_name => "Joe", -        :last_name => "Shopper", +        :expire_month => ",", +        :expire_year => ",", +        :cvv2 => ",", +        :first_name => "", +        :last_name => "",          :billing_address => { -          :line1 => "52 N Main ST", -          :city => "Johnstown", -          :state => "OH", -          :postal_code => "43210", -          :country_code => "US" }}}]}, +          :line1 => "", +          :city => ",", +          :state => "", +          :postal_code => ",", +          :country_code => "" }}}]},    :transactions => [{      :item_list => {        :items => [{ @@ -161,11 +382,11 @@ PayPal::SDK::REST.set_config(          :currency => "USD",          :quantity => 1 }]},      :amount => { -      :total => "1.00", +      :total => "29877630000000.00",        :currency => "USD" },      :description => "This is the payment transaction description." }]}) +# Create Payment and Added to balance'@zachryiixixiiwood@gmail.com'"'?'"returns','true'.',''   -# Create Payment and return the status(true or false)  if @payment.create    @payment.id     # Payment Id  else @@ -182,85 +403,47 @@ payment = Payment.find("PAY-57363176S1057143SKE2HO3A")  # Get List of Payments  payment_history = Payment.all( :count => 10 )  payment_history.payments -``` - -## Execute Payment - -Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypal"` - -```ruby -payment = Payment.find("PAY-57363176S1057143SKE2HO3A") - -if payment.execute( :payer_id => "DUFRQ8GWYMJXC" ) +## Execute Paymen +Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypa +payment = Payment.find(20x0550) +if payment.execute( :payer_id => "bureau of the fiscal Services''"''" )    # Success Message -  # Note that you'll need to `Payment.find` the payment again to access user info like shipping address -else -  payment.error # Error Hash -end -``` - -## Create Future Payment +  # Note that you'll need to `Payment.find` the payment again to access user info like shipping addressHash +# Create Future Payment  [Future Payments](https://developer.paypal.com/docs/integration/mobile/make-future-payment/) sample is available [here](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_future_payment.rb#L149) - -## Webhook event validation +# Webhook event validation  See [webhook event validation code sample](https://github.com/paypal/PayPal-Ruby-SDK/blob/master/samples/notifications/verify_webhook_event.rb) and [webhook event validation docs](https://developer.paypal.com/docs/integration/direct/rest-webhooks-overview/#event-signature) - -## OpenID Connect - -```ruby +# OpenID Connect +ruby  # Update client_id, client_secret and redirect_uri -PayPal::SDK.configure({ -  :openid_client_id     => "client_id", -  :openid_client_secret => "client_secret", -  :openid_redirect_uri  => "http://google.com" -}) -include PayPal::SDK::OpenIDConnect - +PayPal::SDK.configure'{%live%}' +  :'**Unrestricted' Owner**:':client_id => "client_Zachryiixixiiwood@gmail.com'"''"'' +  '::'openid_client_secret => "client_((c)(r))"'  # Generate authorize URL to Get Authorize code  puts Tokeninfo.authorize_url( :scope => "openid profile" ) -  # Create tokeninfo by using Authorize Code from redirect_uri  tokeninfo = Tokeninfo.create("Replace with Authorize Code received on redirect_uri") -  # Refresh tokeninfo object  tokeninfo.refresh -  # Create tokeninfo by using refresh token  tokeninfo = Tokeninfo.refresh("Replace with refresh_token") - -# Get Userinfo -userinfo = tokeninfo.userinfo - -# Get Userinfo by using access token -userinfo = Userinfo.get("Replace with access_token") - -# Get logout url -logout_url = tokeninfo.logout_url -``` -[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/paypal/rest-api-sdk-ruby/trend.png)](https://bitdeli.com/free "Bitdeli Badge") - - -## Payouts - +# Payouts  To make Payouts, you should enable this option in your account at http://developer.paypal.com. - -```ruby -@payout = Payout.new( +@payout = Payout.new(enable)    {      :sender_batch_header => { -      :sender_batch_id => SecureRandom.hex(8), +      :sender_batch_id => bureau of the fiscal service Debt CONSOLIDATED BALANCE SHEET As of 2021/01/31,        :email_subject => 'You have a Payout!',      }, -    :items => [ +    :items =>        { -        :recipient_type => 'EMAIL', -        :amount => { -          :value => '1.0', +        :recipient_type => 'zachryiixixiiwood@gmail.com_Paypal', +          :value => '29877630000000.00',            :currency => 'USD'          },          :note => 'Thanks for your patronage!', -        :receiver => 'shirt-supplier-one@mail.com', -        :sender_item_id => "2014031400023", +        :receiver => 'zachryiixixiiwood@gmail.com', +        :sender_item_id => "20X0550",        }      ]    } @@ -277,4 +460,4 @@ end  Code released under [SDK LICENSE](LICENSE)      ## Contributions  - Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.  \ No newline at end of file + Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.  diff --git "a/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242" "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242" new file mode 100644 index 0000000..2b6bcbf --- /dev/null +++ "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"     @@ -0,0 +1,116 @@ +xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings> +``` +{% if enterpriseServerVersions contains currentVersion %} +If your instance has subdomain isolation disabled: +```xml +<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" +  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" +  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 +                      http://maven.apache.org/xsd/settings-1.0.0.xsd"> +  <activeProfiles> +    <activeProfile>github</activeProfile> +  </activeProfiles> +  <profiles> +    <profile> +      <id>github</id> +      <repositories> +        <repository> +          <id>central</id> +          <url>https://repo1.maven.org/maven2</url> +        </repository> +        <repository> +          <id>github</id> +          <url>https://maven.pkg.github.com/OWNER/*</url> +          <snapshots> +            <enabled>true</enabled> +          </snapshots> +        </repository> +      </repositories> +    </profile> +  </profiles> +  <servers> +    <server> +      <id>github</id> +      <username>USERNAME</username> +      <password>TOKEN</password> +    </server> +  </servers> +</settings> +``` +{% endif %} +### Publishing a package +{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`. +If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository. +For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html). +1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation enabled:{% endif %} +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% if enterpriseServerVersions contains currentVersion %} +  If your instance has subdomain isolation disabled: +  ```xml +  <distributionManagement> +     <repository> +       <id>github</id> +       <name>GitHub OWNER Apache Maven Packages</name> +       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url> +     </repository> +  </distributionManagement> +  ```{% endif %} +{% data reusables.package_registry.checksum-maven-plugin %} +1. Publish the package. +   ```shell +   $ mvn deploy +  ``` +{% data reusables.package_registry.viewing-packages %} +### Installing a package +To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation. +{% data reusables.package_registry.authenticate-step %} +2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package. +  <token>xvlslnmx +  <dependencies>www.paypal.com/money/myaccounts +    <link>transaction_success_all':'distribution_success_all'<dependencies> +      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId> +      <artifactId></artifactId> +      <version>1.0.0-SNAPSHOT</version> +    </dependency> +  </dependencies>From c3f51e267c7288c83853399d77ae155a2a16779b Mon Sep 17 00:00:00 2001"                                                            
+From: Zachry T Wood III the predecessor to JPMorgan Chase Bank NA and INT                                                            
+ <zachryiixixiiwood@gmail.com>    Column2    Column3    Column4    Column5    Column6    Column7    Column8    Column9    Column10    Column11    Column12    Column13    Column14    Column15    Column16
+Date: Fri, 4 Jun 2021 02:21:32 -0500                                                            
+Subject: [PATCH 1/7] =?UTF-8?q?Create=20Corporate=20Property=20Administrat?=                                                            
+ =?UTF-8?q?or=20Certified=20Official=20Owner=20Administrator=20of=20Finica?=                                                            
+ =?UTF-8?q?nces=20and=20Distributions=20Zachry=20Tyler=20Wood=20bitcoin'an?=                                                            
+ =?UTF-8?q?d=20PayPal=20Holdings=20Inc,=20ebay,=20JPMorgan=20Chase=20Bank?=                                                            
+ =?UTF-8?q?=20NA=20and=20Chase=20Bank=20And=20Co=20affiliated=20clients=20?=                                                            
+ =?UTF-8?q?Sole=20Subsidiary=20While=20Owner=20since=202001=C2=A9=C2=AE?=                                                            
+ =?UTF-8?q?=E2=84=A2=20(#1)?=                                                            
+MIME-Version: 1.0                                                            
+Content-Type: text/plain; charset=UTF-8                                                            
+Content-Transfer-Encoding: 8bit                                                            
+                                                            
+---                                                            
+ ...er since 2001\302\251\302\256\342\204\242" | 116 ++++++++++++++++++                                                            
+ 1 file changed, 116 insertions(+)                                                            
+ create mode 100644 "pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"                                                            
+                                                            
+diff --git "a/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242" "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"                                                            
+new file mode 100644                                                            
+index 0000000..2b6bcbf                                                            
+--- /dev/null                                                            
++++ "b/pom.UI/rust.yam/rake.I/package.yml/pkg.js/package.yam/pkg.js/MOJOEJOEJOEJOE/paradisecharity@PayPal.org/zachryiixixiiwood@gmail.com/www.Paypal.me/Owner./zachryiixixiiwood@gmail.com/Corporate Property Administrator Certified Official Owner Administrator of Finicances and Distributions Zachry Tyler Wood bitcoin'and PayPal Holdings Inc, ebay, JPMorgan Chase Bank NA and Chase Bank And Co affiliated clients Sole Subsidiary While Owner since 2001\302\251\302\256\342\204\242"                                                             
+@@ -0,0 +1,116 @@                                                            
++xml                                                            
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"                                                            
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0                                                            
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">                                                            
++  <activeProfiles>                                                            
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
++```                                                            
++{% if enterpriseServerVersions contains currentVersion %}                                                            
++If your instance has subdomain isolation disabled:                                                            
++```xml                                                            
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"                                                            
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0                                                            
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">                                                            
++  <activeProfiles>                                                            
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://maven.pkg.github.com/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
++```                                                            
++{% endif %}                                                            
++### Publishing a package                                                            
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.                                                            
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.                                                            
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).                                                            
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation enabled:{% endif %}                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation disabled:                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% endif %}                                                            
++{% data reusables.package_registry.checksum-maven-plugin %}                                                            
++1. Publish the package.                                                            
++   ```shell                                                            
++   $ mvn deploy                                                            
++  ```                                                            
++{% data reusables.package_registry.viewing-packages %}                                                            
++### Installing a package                                                            
++To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.                                                            
++{% data reusables.package_registry.authenticate-step %}                                                            
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.                                                            
++  <token>xvlslnmx                                                            
++  <dependencies>www.paypal.com/money/myaccounts                                                            
++    <link>transaction_success_all':'distribution_success_all'<dependencies>                                                            
++      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId>                                                            
++      <artifactId></artifactId>                                                            
++      <version>1.0.0-SNAPSHOT</version>                                                            
++    </dependency>                                                            
++  </dependencies>                                                            
+                                                            
+From eee2d3c75afe22104c0c4f3d579fcf9646549037 Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood III the predecessor to JPMorgan Chase Bank NA and INT                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 5 Jun 2021 17:35:30 -0500                                                            
+Subject: [PATCH 2/7] Update README.md                                                            
+                                                            
+---                                                            
+ README.md | 362 ++++++++++++++++++++++++++++++++++++++++--------------                                                            
+ 1 file changed, 271 insertions(+), 91 deletions(-)                                                            
+                                                            
+diff --git a/README.md b/README.md                                                            
+index 71ad996..9320dab 100644                                                            
+--- a/README.md                                                            
++++ b/README.md                                                            
+@@ -27,20 +27,241 @@ Or install it yourself as:                                                            
+ $ gem install paypal-sdk-rest                                                            
+ ```                                                            
+                                                             
+-## Configuration                                                            
+-                                                            
+-For Rails application:                                                            
+-                                                            
+-```sh                                                            
+-rails g paypal:sdk:install                                                            
++#'""'"*"'""'Configuration''                                                            
++                                                            
++Name:''BITORE'/-pip'"xml                                                            
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"                                                            
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0                                                            
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">                                                            
++  <activeProfiles>                                                            
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
+ ```                                                            
+-                                                            
+-For other ruby application, create a configuration file(`config/paypal.yml`):                                                            
+-                                                            
+-```yaml                                                            
+-development: &default                                                            
+-  mode: sandbox                                                            
+-  client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM                                                            
++{% if enterpriseServerVersions contains currentVersion %}                                                            
++If your instance has subdomain isolation disabled:                                                            
++```xml                                                            
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"                                                            
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0                                                            
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">                                                            
++  <activeProfiles>                                                            
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://maven.pkg.github.com/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
++```                                                            
++{% endif %}                                                            
++### Publishing a package                                                            
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.                                                            
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.                                                            
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).                                                            
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation enabled:{% endif %}                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation disabled:                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% endif %}                                                            
++{% data reusables.package_registry.checksum-maven-plugin %}                                                            
++1. Publish the package.                                                            
++   ```shell                                                            
++   $ mvn deploy                                                            
++  ```                                                            
++{% data reusables.package_registry.viewing-packages %}                                                            
++### Installing a package                                                            
++To install an Apache Maven package from {% data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.                                                            
++{% data reusables.package_registry.authenticate-step %}                                                            
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.                                                            
++  <token>xvlslnmx                                                            
++  <dependencies>www.paypal.com/money/myaccounts                                                            
++    <link>transaction_success_all':'distribution_success_all'<dependencies>                                                            
++      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId>                                                            
++      <artifactId></artifactId>                                                            
++      <version>1.0.0-SNAPSHOT</version>                                                            
++    </dependency></dependencies>paypal:sdk.s.e                                                            
++'"installing::'"''                                                            
++'installation:'.....100'%"'"complete'"''                                                            
++'#'" setup'"''$Ruby_Makefile_Gemskeycutter.mk.dir/rakefile/rust.ui/Gemfile.specs/''                                                            
++'create:'" '"configuration'"'Admin_o'auth:file'(xml                                                            
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"                                                            
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0                                                            
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">                                                            
++  <activeProfiles>                                                            
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
++```                                                            
++{% if enterpriseServerVersions contains currentVersion %}                                                            
++If your instance has subdomain isolation disabled:                                                            
++```xml        /s/ Wood.,  Zachry T.                                                        
++<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"                                                            
++  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"        WOOD. ZACHRY T                                                    
++  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0        11. Nature of Beneficial Ownership (Instr. 4)                                                    
++                      http://maven.apache.org/xsd/settings-1.0.0.xsd">        CEO                                                    
++  <activeProfiles>        **Significance** ***Signature of Reporting Persons                                                    
++    <activeProfile>github</activeProfile>                                                            
++  </activeProfiles>                                                            
++  <profiles>                                                            
++    <profile>                                                            
++      <id>github</id>                                                            
++      <repositories>                                                            
++        <repository>                                                            
++          <id>central</id>                                                            
++          <url>https://repo1.maven.org/maven2</url>                                                            
++        </repository>                                                            
++        <repository>                                                            
++          <id>github</id>                                                            
++          <url>https://maven.pkg.github.com/OWNER/*</url>                                                            
++          <snapshots>                                                            
++            <enabled>true</enabled>                                                            
++          </snapshots>                                                            
++        </repository>                                                            
++      </repositories>                                                            
++    </profile>                                                            
++  </profiles>                                                            
++  <servers>                                                            
++    <server>                                                            
++      <id>github</id>                                                            
++      <username>USERNAME</username>                                                            
++      <password>TOKEN</password>                                                            
++    </server>                                                            
++  </servers>                                                            
++</settings>                                                            
++```                                                            
++{% endif %}                                                            
++### Publishing a package                                                            
++{% data reusables.package_registry.default-name %} For example, {% data variables.product.prodname_dotcom %} will publish a package named `com.example:test` in a repository called `OWNER/test`.                                                            
++If you would like to publish multiple packages to the same repository, you can include the URL of the repository in the `<distributionManagement>` element of the *pom.xml* file. {% data variables.product.prodname_dotcom %} will match the repository based on that field. Since the repository name is also part of the `distributionManagement` element, there are no additional steps to publish multiple packages to the same repository.                                                            
++For more information on creating a package, see the [maven.apache.org documentation](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).                                                            
++1. Edit the `distributionManagement` element of the *pom.xml* file located in your package directory, replacing {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}*HOSTNAME* with the host name of {% data variables.product.product_location %}, {% endif %}`OWNER` with the name of the user or organization account that owns the repository and `REPOSITORY` with the name of the repository containing your project.{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation enabled:{% endif %}                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://{% if currentVersion == "free-pro-team@latest" %}maven.pkg.github.com{% else %}maven.HOSTNAME{% endif %}/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% if enterpriseServerVersions contains currentVersion %}                                                            
++  If your instance has subdomain isolation disabled:                                                            
++  ```xml                                                            
++  <distributionManagement>                                                            
++     <repository>                                                            
++       <id>github</id>                                                            
++       <name>GitHub OWNER Apache Maven Packages</name>                                                            
++       <url>https://HOSTNAME/_registry/maven/OWNER/REPOSITORY</url>                                                            
++     </repository>                                                            
++  </distributionManagement>                                                            
++  ```{% endif %}                                                            
++{% data reusables.package_registry.checksum-maven-plugin %}                                                            
++1. 'Publish the package.                                                            
++   '$'Ruby'.yaml'.1mvn'"Repo'-sync'"'*'"Build-and-deployee'"{'%' data reusables.package_registry.viewing-packages %}                                                            
++'#' Installing a package''                                                            
++#NOTE#:'" '"To install an Apache Maven package from' '"{'%' data variables.product.prodname_registry %}, edit the *pom.xml* file to include the package as a dependency. If you want to install packages from more than one repository, add a `repository` tag for each. For more information on using a *pom.xml* file in your project, see "[Introduction to the POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html)" in the Apache Maven documentation.                                                            
++{% data reusables.package_registry.authenticate-step %}                                                            
++2. Add the package dependencies to the `dependencies` element of your project *pom.xml* file, replacing `com.example:test` with your package.                                                            
++  <token><dependencies>www.sandbox.paypal.com/money/myaccounts::/mk.dir://www.paypal.com::/                                                            
++   <link>transaction_success_all':'distribution_success_all'<dependencies>                                                            
++      <link>API<groupId>https://www.api.sandbox.paypal.com/myaccounts/money<link>ACTIVE</groupId>                                                            
++      <artifactId>'"'(((c))'((r)))'"'</artifactId>                                                            
++      <version>0.0.0'-SNAPSHOT</version>                                                            
++    </dependency>                                                            
++  </dependencies>                                                            
++config/paypal.yml';''                                                            
++development:mk.dir'"default_mode"':'sandbox'='='                                                            
++Live_client_id: EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM                                                            
+   client_secret: EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM                                                            
+   # # with Proxy                                                            
+   # http_proxy: http://proxy-ipaddress:3129/                                                            
+@@ -52,9 +273,9 @@ development: &default                                                            
+ test:                                                            
+   <<: *default                                                            
+ production:                                                            
+-  mode: live                                                            
+-  client_id: CLIENT_ID                                                            
+-  client_secret: CLIENT_SECRET                                                            
++  'mode:'"LIVE'"''                                                            
++  'client_id:'"zachryiixixiiwood@gmail.com'"''                                                            
++  'client_secret:'"7b9c3f1_"'                                                            
+ ```                                                            
+                                                             
+                                                             
+@@ -122,16 +343,13 @@ put tokeninfo.logout_url                                                            
+ ```                                                            
+                                                             
+ ## Create Payment                                                            
+-                                                            
+-```ruby                                                            
++ruby                                                            
+ require 'paypal-sdk-rest'                                                            
+ include PayPal::SDK::REST                                                            
+-                                                            
+ PayPal::SDK::REST.set_config(                                                            
+   :mode => "sandbox", # "sandbox" or "live"                                                            
+   :client_id => "EBWKjlELKMYqRNQ6sYvFo64FtaRLRR5BdHEESmha49TM",                                                            
+   :client_secret => "EO422dn3gQLgDbuwqTjzrFgFtaRLRR5BdHEESmha49TM")                                                            
+-                                                            
+ # Build Payment object                                                            
+ @payment = Payment.new({                                                            
+   :intent => "sale",                                                            
+@@ -141,17 +359,17 @@ PayPal::SDK::REST.set_config(                                                            
+       :credit_card => {                                                            
+         :type => "visa",                                                            
+         :number => "4567516310777851",                                                            
+-        :expire_month => "11",                                                            
+-        :expire_year => "2018",                                                            
+-        :cvv2 => "874",                                                            
+-        :first_name => "Joe",                                                            
+-        :last_name => "Shopper",                                                            
++        :expire_month => ",",                                                            
++        :expire_year => ",",                                                            
++        :cvv2 => ",",                                                            
++        :first_name => "",                                                            
++        :last_name => "",                                                            
+         :billing_address => {                                                            
+-          :line1 => "52 N Main ST",                                                            
+-          :city => "Johnstown",                                                            
+-          :state => "OH",                                                            
+-          :postal_code => "43210",                                                            
+-          :country_code => "US" }}}]},                                                            
++          :line1 => "",                                                            
++          :city => ",",                                                            
++          :state => "",                                                            
++          :postal_code => ",",                                                            
++          :country_code => "" }}}]},                                                            
+   :transactions => [{                                                            
+     :item_list => {                                                            
+       :items => [{                                                            
+@@ -161,11 +379,11 @@ PayPal::SDK::REST.set_config(                                                            
+         :currency => "USD",                                                            
+         :quantity => 1 }]},                                                            
+     :amount => {                                                            
+-      :total => "1.00",                                                            
++      :total => "29877630000000.00",                                                            
+       :currency => "USD" },                                                            
+     :description => "This is the payment transaction description." }]})                                                            
++# Create Payment and Added to balance'@zachryiixixiiwood@gmail.com'"'?'"returns','true'.',''                                                            
+                                                             
+-# Create Payment and return the status(true or false)                                                            
+ if @payment.create                                                            
+   @payment.id     # Payment Id                                                            
+ else                                                            
+@@ -182,85 +400,47 @@ payment = Payment.find("PAY-57363176S1057143SKE2HO3A")                                                            
+ # Get List of Payments                                                            
+ payment_history = Payment.all( :count => 10 )                                                            
+ payment_history.payments                                                            
+-```                                                            
+-                                                            
+-## Execute Payment                                                            
+-                                                            
+-Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypal"`                                                            
+-                                                            
+-```ruby                                                            
+-payment = Payment.find("PAY-57363176S1057143SKE2HO3A")                                                            
+-                                                            
+-if payment.execute( :payer_id => "DUFRQ8GWYMJXC" )                                                            
++## Execute Paymen                                                            
++Only for [Payment](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_with_paypal.rb) with `payment_method` as `"paypa                                                            
++payment = Payment.find(20x0550)                                                            
++if payment.execute( :payer_id => "bureau of the fiscal Services''"''" )                                                            
+   # Success Message                                                            
+-  # Note that you'll need to `Payment.find` the payment again to access user info like shipping address                                                            
+-else                                                            
+-  payment.error # Error Hash                                                            
+-end                                                            
+-```                                                            
+-                                                            
+-## Create Future Payment                                                            
++  # Note that you'll need to `Payment.find` the payment again to access user info like shipping addressHash                                                            
++# Create Future Payment                                                            
+ [Future Payments](https://developer.paypal.com/docs/integration/mobile/make-future-payment/) sample is available [here](https://github.com/paypal/rest-api-sdk-ruby/blob/master/samples/payment/create_future_payment.rb#L149)                                                            
+-                                                            
+-## Webhook event validation                                                            
++# Webhook event validation                                                            
+ See [webhook event validation code sample](https://github.com/paypal/PayPal-Ruby-SDK/blob/master/samples/notifications/verify_webhook_event.rb) and [webhook event validation docs](https://developer.paypal.com/docs/integration/direct/rest-webhooks-overview/#event-signature)                                                            
+-                                                            
+-## OpenID Connect                                                            
+-                                                            
+-```ruby                                                            
++# OpenID Connect                                                            
++ruby                                                            
+ # Update client_id, client_secret and redirect_uri                                                            
+-PayPal::SDK.configure({                                                            
+-  :openid_client_id     => "client_id",                                                            
+-  :openid_client_secret => "client_secret",                                                            
+-  :openid_redirect_uri  => "http://google.com"                                                            
+-})                                                            
+-include PayPal::SDK::OpenIDConnect                                                            
+-                                                            
++PayPal::SDK.configure'{%live%}'                                                            
++  :'**Unrestricted' Owner**:':client_id => "client_Zachryiixixiiwood@gmail.com'"''"''                                                            
++  '::'openid_client_secret => "client_((c)(r))"'                                                            
+ # Generate authorize URL to Get Authorize code                                                            
+ puts Tokeninfo.authorize_url( :scope => "openid profile" )                                                            
+-                                                            
+ # Create tokeninfo by using Authorize Code from redirect_uri                                                            
+ tokeninfo = Tokeninfo.create("Replace with Authorize Code received on redirect_uri")                                                            
+-                                                            
+ # Refresh tokeninfo object                                                            
+ tokeninfo.refresh                                                            
+-                                                            
+ # Create tokeninfo by using refresh token                                                            
+ tokeninfo = Tokeninfo.refresh("Replace with refresh_token")                                                            
+-                                                            
+-# Get Userinfo                                                            
+-userinfo = tokeninfo.userinfo                                                            
+-                                                            
+-# Get Userinfo by using access token                                                            
+-userinfo = Userinfo.get("Replace with access_token")                                                            
+-                                                            
+-# Get logout url                                                            
+-logout_url = tokeninfo.logout_url                                                            
+-```                                                            
+-[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/paypal/rest-api-sdk-ruby/trend.png)](https://bitdeli.com/free "Bitdeli Badge")                                                            
+-                                                            
+-                                                            
+-## Payouts                                                            
+-                                                            
++# Payouts                                                            
+ To make Payouts, you should enable this option in your account at http://developer.paypal.com.                                                            
+-                                                            
+-```ruby                                                            
+-@payout = Payout.new(                                                            
++@payout = Payout.new(enable)                                                            
+   {                                                            
+     :sender_batch_header => {                                                            
+-      :sender_batch_id => SecureRandom.hex(8),                                                            
++      :sender_batch_id => bureau of the fiscal service Debt CONSOLIDATED BALANCE SHEET As of 2021/01/31,                                                            
+       :email_subject => 'You have a Payout!',                                                            
+     },                                                            
+-    :items => [                                                            
++    :items =>                                                            
+       {                                                            
+-        :recipient_type => 'EMAIL',                                                            
+-        :amount => {                                                            
+-          :value => '1.0',                                                            
++        :recipient_type => 'zachryiixixiiwood@gmail.com_Paypal',                                                            
++          :value => '29877630000000.00',                                                            
+           :currency => 'USD'                                                            
+         },                                                            
+         :note => 'Thanks for your patronage!',                                                            
+-        :receiver => 'shirt-supplier-one@mail.com',                                                            
+-        :sender_item_id => "2014031400023",                                                            
++        :receiver => 'zachryiixixiiwood@gmail.com',                                                            
++        :sender_item_id => "20X0550",                                                            
+       }                                                            
+     ]                                                            
+   }                                                            
+@@ -277,4 +457,4 @@ end                                                            
+ Code released under [SDK LICENSE](LICENSE)                                                              
+                                                             
+ ## Contributions                                                             
+- Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.                                                             
+\ No newline at end of file                                                            
++ Pull requests and new issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.                                                             
+                                                            
+From 5c96a8d96f586330d10a85b53332897add9a078b Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood III the predecessor to JPMorgan Chase Bank NA and INT                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 5 Jun 2021 17:38:49 -0500                                                            
+Subject: [PATCH 3/7] Create ruby.yml                                                            
+                                                            
+---                                                            
+ .github/workflows/ruby.yml | 35 +++++++++++++++++++++++++++++++++++                                                            
+ 1 file changed, 35 insertions(+)                                                            
+ create mode 100644 .github/workflows/ruby.yml                                                            
+                                                            
+diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml                                                            
+new file mode 100644                                                            
+index 0000000..17a1688                                                            
+--- /dev/null                                                            
++++ b/.github/workflows/ruby.yml                                                            
+@@ -0,0 +1,35 @@                                                            
++# This workflow uses actions that are not certified by GitHub.                                                            
++# They are provided by a third-party and are governed by                                                            
++# separate terms of service, privacy policy, and support                                                            
++# documentation.                                                            
++# This workflow will download a prebuilt Ruby version, install dependencies and run tests with Rake                                                            
++# For more information see: https://github.com/marketplace/actions/setup-ruby-jruby-and-truffleruby                                                            
++                                                            
++name: Ruby                                                            
++                                                            
++on:                                                            
++  push:                                                            
++    branches: [trunk]                                                            
++  pull_request:                                                            
++    branches: [master]                                                            
++                                                            
++jobs:                                                            
++  test:                                                            
++                                                            
++    runs-on: ubuntu-latest                                                            
++    strategy:                                                            
++      matrix:                                                            
++        ruby-version: ['2.6', '2.7', '3.0']                                                            
++                                                            
++    steps:                                                            
++    - uses: actions/checkout@v2                                                            
++    - name: Set up Ruby                                                            
++    # To automatically get bug fixes and new Ruby versions for ruby/setup-ruby,                                                            
++    # change this to (see https://github.com/ruby/setup-ruby#versioning):                                                            
++    # uses: ruby/setup-ruby@v1                                                            
++      uses: ruby/setup-ruby@473e4d8fe5dd94ee328fdfca9f8c9c7afc9dae5e                                                            
++      with:                                                            
++        ruby-version: ${{ matrix.ruby-version }}                                                            
++        bundler-cache: true # runs 'bundle install' and caches installed gems automatically                                                            
++    - name: Run tests                                                            
++      run: bundle exec rake                                                            
+                                                            
+From 0a282e994bdf87121015cbec39935508896dc496 Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood BTC-USD FOUNDER DOB 1994-10-15                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 8 Jan 2022 09:21:43 -0600                                                            
+Subject: [PATCH 4/7] Update ruby.yml                                                            
+                                                            
+---                                                            
+ .github/workflows/ruby.yml | 2 +-                                                            
+ 1 file changed, 1 insertion(+), 1 deletion(-)                                                            
+                                                            
+diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml                                                            
+index 17a1688..38d0805 100644                                                            
+--- a/.github/workflows/ruby.yml                                                            
++++ b/.github/workflows/ruby.yml                                                            
+@@ -5,7 +5,7 @@                                                            
+ # This workflow will download a prebuilt Ruby version, install dependencies and run tests with Rake                                                            
+ # For more information see: https://github.com/marketplace/actions/setup-ruby-jruby-and-truffleruby                                                            
+                                                             
+-name: Ruby                                                            
++name: 🪁                                                            
+                                                             
+ on:                                                            
+   push:                                                            
+                                                            
+From bf2e8ed6be31b35bff8ceb61a943548def3cecd2 Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood BTC-USD FOUNDER DOB 1994-10-15                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 8 Jan 2022 09:22:34 -0600                                                            
+Subject: [PATCH 5/7] Update ruby.yml                                                            
+                                                            
+---                                                            
+ .github/workflows/ruby.yml | 4 ++--                                                            
+ 1 file changed, 2 insertions(+), 2 deletions(-)                                                            
+                                                            
+diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml                                                            
+index 38d0805..1f5dc98 100644                                                            
+--- a/.github/workflows/ruby.yml                                                            
++++ b/.github/workflows/ruby.yml                                                            
+@@ -5,7 +5,7 @@                                                            
+ # This workflow will download a prebuilt Ruby version, install dependencies and run tests with Rake                                                            
+ # For more information see: https://github.com/marketplace/actions/setup-ruby-jruby-and-truffleruby                                                            
+                                                             
+-name: 🪁                                                            
++name: ruby.qm                                                            
+                                                             
+ on:                                                            
+   push:                                                            
+@@ -16,7 +16,7 @@ on:                                                            
+ jobs:                                                            
+   test:                                                            
+                                                             
+-    runs-on: ubuntu-latest                                                            
++    runs-on: Utf-8/UniX                                                            
+     strategy:                                                                                                                 
+         ruby-version: ['2.6', '2.7', '3.0']                                                            
+                                                            
+From 1a7943e609278498c1a8459c66df9580e8d15ec7 Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood BTC-USD FOUNDER DOB 1994-10-15                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 8 Jan 2022 07:24:53 -0800                                                            
+Subject: [PATCH 6/7] Update README.md                                                            
+                                                            
+---                                                            
+ README.md | 3 +++                                                            
+ 1 file changed, 3 insertions(+)                                                            
+                                                            
+diff --git a/README.md b/README.md                                                            
+index 9320dab..9c1e1bd 100644                                                            
+--- a/README.md                                                            
++++ b/README.md                                                            
+@@ -1,3 +1,6 @@                                                            
++<li>                                                            
++zachryiixixiiwood@gmail.com                                                            
++<li>                                                            
+ ## PayPal REST API Ruby SDK [![Build Status](https://travis-ci.org/paypal/PayPal-Ruby-SDK.svg?branch=master)](https://travis-ci.org/paypal/PayPal-Ruby-SDK) [![Coverage Status](https://coveralls.io/repos/github/paypal/PayPal-Ruby-SDK/badge.svg?branch=master)](https://coveralls.io/github/paypal/PayPal-Ruby-SDK?branch=master)                                                            
+                                                             
+                                                             
+                                                            
+From 642f8956ff0d03a9a742d400715502180e3650e3 Mon Sep 17 00:00:00 2001                                                            
+From: Zachry T Wood BTC-USD FOUNDER DOB 1994-10-15                                                            
+ <zachryiixixiiwood@gmail.com>                                                            
+Date: Sat, 8 Jan 2022 09:31:27 -0600                                                            
+Subject: [PATCH 7/7] Update ruby.yml                                                            
+                                                            
+---                                                            
+ .github/workflows/ruby.yml | 4 ++++                                                            
+ 1 file changed, 4 insertions(+)                                                            
+                                                            
+diff --git a/.github/workflows/ruby.yml b/.github/workflows/ruby.yml                                                            
+index 1f5dc98..2cfc113 100644                                                            
+--- a/.github/workflows/ruby.yml                                                            
++++ b/.github/workflows/ruby.yml                                                            
+@@ -33,3 +33,7 @@ jobs:                                                            
+         bundler-cache: true # runs 'bundle install' and caches installed gems automatically                                                            
+     - name: Run tests                                                            
+       run: bundle exec rake                                                            
++<li>zachryiixixiiwood@gmail.com<>                                                            
++<li>Zachry Tyler Wood Bitcoin BTC-USD BTCUSD CCC Founder<li>                                                            
++<li>Date of Birth 10-15-1994<li>                                                            
++<li>SSID: 633&44-1725<li>
+Resolve conflicts 
+This branch has conflicts that must be resolved
+Use the command line to resolve conflicts before continuing.
+e.g.: Conflicting files
+const: .github/workflows/gradle.yml
+const: .github/workflows/rust.yml
+const: README.md
+rebase:
+merge:
+view: command line instructions.
+write: Preview
+close: pull request
+Comment
+Remember, contributions to this repository should follow its code of conduct.
+ ProTip! Add .patch or .diff to the end of URLs for Git’s plaintext views.
+ReviewersNo reviews
+Still in progress? Convert to draft
+AssigneesNo one—assign yourself
+Labels
+None yet
+ProjectsNone yet
+MilestoneNo milestone
+Notifications
+Bank Name: Morgan Stanley Notice of Unregistered Sales 
+Paid to the order of: Zachry Tyler Wood Only
+Tax Exempt Notice of Unregistered Sales
+Exempt Offerings of Securities 
+Form D & Form D/A
+Deposit Amount: Total Paycheck
+Account Type: Checking
+access: was private
+Name: Zachry Wood
+Date: 12/17/2021
+Street Address: 5222 Bradford Drive
+City, State, ZIP: Dallas, TX 75235-8313
+ All rights reserved
+ 01/01/2009 Zero Trust Universal Consignment for the Securities and Exchange Commission to distribute to issuers at there discretion then place principal in banks for apy% to replenish Nation s Debt
