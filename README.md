# EFZP
Parse an email to get properties like salutation, body, signature, reply. These properties are like "zones" in an email, thus the name Email Functional Zone Parser.

Input:

```
"Hi Dave,\nLets meet up this Tuesday\nCheers, Tom\n\nOn Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: Hey Tom,\nHow about we get together ..."
```

Output:

```
{
	"Salutation": "Hi Dave,\n"
	"Body": "Lets meet up this Tuesday\n"
	"Signature": "Cheers, Tom\n\n"
	"Reply Text": "On Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: ..."
}
```

### Installation

```bash
git clone https://github.com/mschmidoev/EFZP_python3.git
```

### Usage

This python script

```python
import EFZP as zp
p = zp.parse("Hi Dave,\nLets meet up this Tuesday\nCheers, Tom\n\nOn Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: Hey Tom,\nHow about we get together ...")
print p

```

prints this

```
{'salutation': 'Hi Dave,\n', 'body': 'Lets meet up this Tuesday\n', 'reply_text': 'On Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: Hey Tom,\nHow about we get together ...', 'signature': 'Cheers, Tom\n\n'}
```
