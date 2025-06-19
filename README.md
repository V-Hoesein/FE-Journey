# FE Note


### Case: event Propagation
Mengetikan nama item baru pada komponen Dropdown menu yang memiliki utilitas add new item dengan input field
### Story: 
Ketika Dropdown sudah memiliki list menu di dalamnya [mangga, apel, jeruk], lalu melakukan _add new item_ dan mengetikan nama item ex:jambu input field kehilangan fokus karena ada menu awalan 'j', hal ini disebut typeahead conflict. Atasi dengan alternatif: event stop propagation ```<div onKeyDown={e => e.stopPropagation()}>```

<hr/>
