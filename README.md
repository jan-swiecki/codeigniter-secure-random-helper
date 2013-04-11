## CodeIgniter-Secure-Random-Helper

`random_string` from [String helper](http://ellislab.com/codeigniter/user-guide/helpers/string_helper.html) equivalent, but cryptographically secure.

### Install

Put `secure_random_helper.php` into `your_project/application/helpers/`.

### Usage

```php
class Home extends CI_Controller
{
	public function index()
	{
		// $this->load->helper('string');
		$this->load->helper('secure_random');

		// $password = random_string('alnum', 8);
		$password = secure_random_string('alnum', 8);
	}	
}
```

Note: `secure_random_string` will throw `Exception` if generated string was not secure (see `$crypto_strong` argument of [openssl_random_pseudo_bytes](php.net/openssl_random_pseudo_bytes) function).


### Credits

Christophe comment on [php.net](http://php.net/manual/en/function.openssl-random-pseudo-bytes.php#104322)
