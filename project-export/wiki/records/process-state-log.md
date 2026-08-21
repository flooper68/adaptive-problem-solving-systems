# Process state log

Append-only history of process signal readings taken by retrospectives. One entry per retrospective, in the fixed shape below so entries can be compared by eye. Entries are appended with `append_wiki_file` against the current page SHA and never edited. Process pages remain the compiled knowledge; this log preserves what was read and decided.

Entry shape:

    ## <date> — <process> — <session key>
    Page: <sha before> → <sha after, or unchanged>   Window: <sessions read>
    Reading: completed n/n · steps covered n/n · corrections n · decisions held n/n · expected effects met n / missed n / unreadable n · reported failures n
    Compared with <previous entry>: better | worse | same | unreadable — <one line why>
    Worked: (1) <finding> → <edit> · expect: <checkable effect>
    Parked: <finding> (<why below the cut>; admit when <trigger>)
    Handoffs: <to grooming or brainstorming, or none>
    Next: <trigger>

## Entries
