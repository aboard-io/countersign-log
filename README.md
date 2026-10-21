# Countersign public log

Copies of the public log of [Countersign](https://countersign.tinylittleoffice.com), one file a day, committed by
Countersign's server just after midnight UTC: `log/YYYY-MM-DD.txt` is the log as it stood at the end of that day.
Each commit's hash pins the file's bytes, GitHub's clock dates the commit, and every signed PDF Countersign mails
names the log, so anyone holding one can check that the document with its fingerprint was signed by then.

Each file is plain text: a header naming the server's key and what an entry signs, then one tab-separated line an
entry (`seq at signing fingerprint pages prev csig hash`), then the addresses of earlier days' copies here. Entries
are chained (`prev` is the SHA-256 of the entry before, countersignature included) and countersigned by the key
published at https://countersign.tinylittleoffice.com/.well-known/countersign.json. No entry names a person, a
title or a word of a document: the signing's id, the document's fingerprint, its page count, the time and the
signed copy's SHA-256 alone.

How to check a copy: https://countersign.tinylittleoffice.com/about/ · For programs: https://countersign.tinylittleoffice.com/llms.txt

Made by [Aboard](https://aboard.com).
