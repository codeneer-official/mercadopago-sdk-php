# Mercado Pago SDK for PHP for Symfony 5
### That is a forked project for improve use in Symfony 5 application


## 🌟 Getting Started
  
  Simple usage looks like:
  
```php
  <?php
    require_once 'vendor/autoload.php'; // You have to require the library from your Composer vendor folder

    MercadoPago\SDK::setAccessToken("YOUR_ACCESS_TOKEN"); // Either Production or SandBox AccessToken

    $payment = new MercadoPago\Payment();
    
    $payment
      ->setTransactionAmount(141)
      ->setToken("YOUR_CARD_TOKEN")
      ->setDescription("Ergonomic Silk Shirt")
      ->setInstallments(1)
      ->setPaymentMethodId("visa")
      ->setPayer([
        "email" => "larue.nienow@email.com"
      ])
    ;

    $payment->save();

    echo $payment->getStatus();
  ?>
```
