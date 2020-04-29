# EmailParser

This Repo is forked from [Trindaz](https://github.com/Trindaz/EFZP)</br>
Parse an email to get properties like salutation, body, signature, reply.

### Installation

```bash
git clone https://github.com/Vinay26k/EmailParser.git
```

### Usage

```python
import EmailParser as ep
p = ep.parse("Hi Dave,\nLets meet up this Tuesday\nCheers, Tom\n\nOn Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: Hey Tom,\nHow about we get together ...")
print(p)

```

prints this

```json
{
    "salutation": "Hi Dave,\n",
    "body": "Lets meet up this Tuesday\n",
    "reply_text": "On Sunday, 15 May 2011 at 5:02 PM, Dave Trindall wrote: Hey Tom,\nHow about we get together ...",
    "signature": "Cheers, Tom\n\n"
}
```
