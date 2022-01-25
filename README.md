# Indodax-machine
It’s a bot using simple feature  - jangan keseringan make (haram cok)

# Example of Request PHP (API-PANAS)
## Get Info
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
	$data = [
	        'method' => 'getInfo',
	        'timestamp' => '1578304294000',
	        'recvWindow' => '1578303937000'
	    ];
	$post_data = http_build_query($data, '', '&');
    $sign = hash_hmac('sha512', $post_data, $secretKey);
    
    $headers = ['Key:'.$key,'Sign:'.$sign];

    $curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_HTTPHEADER => $headers,
        CURLOPT_URL => $url,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => $data,
        CURLOPT_RETURNTRANSFER => true
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    echo $response;
```

## Transaction History
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
	$data = [
        'method' => 'transHistory',
        'timestamp' => '1578304294000',
        'recvWindow' => '1578303937000'
    ];
	$post_data = http_build_query($data, '', '&');
    $sign = hash_hmac('sha512', $post_data, $secretKey);

    $headers = ['Key:'.$key,'Sign:'.$sign];

    $curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_HTTPHEADER => $headers,
        CURLOPT_URL => $url,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => $data,
        CURLOPT_RETURNTRANSFER => true
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    echo $response;
```

## Trade
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
	$data = [
        'method' => 'trade',
        'timestamp' => '1578304294000',
        'recvWindow' => '1578303937000',
        'pair' => 'btc_idr',
        'type' => 'sell',
        'price' => '107202000',
        'idr' => '',
        'btc' => '0.00313482'
    ];
	$post_data = http_build_query($data, '', '&');
    $sign = hash_hmac('sha512', $post_data, $secretKey);

    $headers = ['Key:'.$key,'Sign:'.$sign];

    $curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_HTTPHEADER => $headers,
        CURLOPT_URL => $url,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => $data,
        CURLOPT_RETURNTRANSFER => true
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    echo $response;
```

## Trade History
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
    $data = [
        'method' => 'tradeHistory',
        'timestamp' => '1578304294000',
        'recvWindow' => '1578303937000',
        'count' => '',
        'from_id' => '',
        'end_id' => '',
        'order' => '',
        'since' => '',
        'end' => '',
        'pair' => ''
    ];
    $post_data = http_build_query($data, '', '&');
    $sign = hash_hmac('sha512', $post_data, $secretKey);

    $headers = ['Key:'.$key,'Sign:'.$sign];

    $curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_HTTPHEADER => $headers,
        CURLOPT_URL => $url,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => $data,
        CURLOPT_RETURNTRANSFER => true
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    echo $response;
```

## Open Orders
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
	$data = [
        'method' => 'openOrders',
        'timestamp' => '1578304294000',
        'recvWindow' => '1578303937000',
        'pair' => 'btc_idr'
    ];
	$post_data = http_build_query($data, '', '&');
    $sign = hash_hmac('sha512', $post_data, $secretKey);

    $headers = ['Key:'.$key,'Sign:'.$sign];

    $curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_HTTPHEADER => $headers,
        CURLOPT_URL => $url,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => $data,
        CURLOPT_RETURNTRANSFER => true
    ));

    $response = curl_exec($curl);

    curl_close($curl);
    echo $response;
```

## Order History
Sample code below :
```php
<?php
    $url = 'https://indodax.com/tapi';
    // Please find Key from trade API Indodax exchange
    $key = '****';
    // Please find Secret Key from trade API Indodax exchange
    $secretKey = '****';
    
	$data = [
        'method' => 'orderHistory',
        'timestamp' => '1578304294000',
        'recvWindow' => '1578303937000',
        'pair' => 'btc_idr',
        'count' => '',
