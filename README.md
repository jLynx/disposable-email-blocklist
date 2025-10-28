# Disposable Email Domains

A simple list of disposable and temporary email domains.

## Usage

**Raw list URL:**

https://raw.githubusercontent.com/jLynx/disposable-email-domains/main/domains.txt

### Examples

**Python:**

```python
import requests

domains = requests.get('https://raw.githubusercontent.com/YOUR-USERNAME/disposable-email-domains/main/domains.txt').text.splitlines()
blocked = set(domains)

email_domain = email.split('@')[1].lower()
if email_domain in blocked:
    print("Disposable email detected")
```

**JavaScript:**

```javascript
fetch(
  "https://raw.githubusercontent.com/YOUR-USERNAME/disposable-email-domains/main/domains.txt"
)
  .then((r) => r.text())
  .then((data) => {
    const blocked = new Set(data.split("\n"))
    // Check: blocked.has(domain)
  })
```

**PHP:**

```php
$domains = file('https://raw.githubusercontent.com/YOUR-USERNAME/disposable-email-domains/main/domains.txt', FILE_IGNORE_NEW_LINES);
$blocked = array_flip($domains);

if (isset($blocked[$domain])) {
    // Disposable email
}
```

## Contributing

Add new domains via pull request. Keep domains:

- Lowercase
- One per line
- Alphabetically sortedS
