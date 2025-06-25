# FE Journal untuk reminder azz


### Case: event Propagation
Mengetikan nama item baru pada komponen Dropdown menu yang memiliki utilitas add new item dengan input field
### Story: 
Ketika Dropdown sudah memiliki list menu di dalamnya [mangga, apel, jeruk], lalu melakukan _add new item_ dan mengetikan nama item ex:jambu input field kehilangan fokus karena ada menu awalan 'j', hal ini disebut typeahead conflict. Atasi dengan alternatif: event stop propagation ```<div onKeyDown={e => e.stopPropagation()}>```

<hr/>

### Case: Menggunakan Server Action NextJS
Jadi kemarin aku coba gunain server action di next untuk post data ke be nya tuh, tpi di form fe nya itu aku pake validasi RHF ama zod. nah aing mah pake form dari [shadcn/form](https://ui.shadcn.com/docs/components/form) jadi validasinya ntuh live di FE dan submitnya ntuh dari form :   ```<form onSubmit={form.handleSubmit(onSubmit)}>``` dan hit ke ```function onSubmit(values: z.infer<typeof formSchema>) { #disini action dari be actionc nya }``` nah gini tuh gabisa untuk server action, whyyyy? karena klo mau pake server action harus pake form native jadinya formnya ntuh ```<form action={#nah disini action server nya}>``` jadi yang di kirim ke fungsi actionnya itu formData bentuknya, page formnya bisa pake useFormAction & useFormStatus btw
