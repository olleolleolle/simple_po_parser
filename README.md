# Simple Po Parser

This is a simple PO file to ruby hash parser, which complies with [GNU PO file specification](https://www.gnu.org/software/gettext/manual/html_node/PO-Files.html). Tested with the msgcat (GNU gettext-tools) 0.18.3 tool.

## Hash format

A PO message is parsed into a hash with meaningful keys for each type of line.
The values are always arrays of strings.
Each string is representing one line of content in the PO file.

```ruby
{
  :translator_comment => [""],
  :extracted_comment => [""],
  :reference => [""],
  :flag => [""],
  :previous_msgctxt => [""], # msgctxt of the message used for the fuzzy translation
  :previous_msgid => [""], # msgid of the messaged used for the fuzzy translation
  :previous_msgid_plural => [""],
  :msgctxt => [""],
  :msgid => [""],
  :msgid_plural => [""],
  :msgstr => [""], # for singular messages
  "msgstr[N]" => [""] # for plural messages, there N is the plural number starting from 0
}
```

### License

License: [MIT](LICENSE.txt) - Copyright (c) 2017 Dennis-Florian Herr @Experteer GmbH
