<script>
	import Pager from './Pager.svelte';

	let contents = [
		{id: 0, content:`<p>Excerpt from</p><h1>ALICE'S ADVENTURES<br>
IN WONDERLAND</h1><p>By Lewis Carroll</p>`},
			{id: 1, content:`<p>The Caterpillar and Alice looked
at each other for some time in
silence: at last the Caterpillar took
the hookah out of its mouth, and
addressed her in a languid, sleepy voice.</p>

<p>"Who are <i>you?</i>" said the Caterpillar.</p>

<p>This was not an encouraging opening for a
conversation. Alice replied, rather shyly, "I
hardly know, sir, just at present—at least I
know who I <i>was</i> when I got up this morning,
but I think I must have been changed several
times since then."</p>

<p>"What do you mean by that?" said the
Caterpillar sternly. "Explain yourself!"</p>

<p>"I can't explain <i>myself</i>, I'm afraid, sir,"
said Alice, "because I'm not myself, you see."</p>

<p>"I don't see," said the Caterpillar.</p>`},
		{id: 2, content:`<p>"I'm afraid I can't put it more clearly,"
Alice replied very politely, "for I can't understand
it myself to begin with; and being so
many different sizes in a day is very confusing."</p>

<p>"It isn't," said the Caterpillar.</p>

<p>"Well, perhaps you haven't found it so
yet," said Alice, "but when you have to turn
into a chrysalis—you will some day, you
know—and then after that into a butterfly, I
should think you'll feel it a little queer, won't
you?"</p>

<p>"Not a bit," said the Caterpillar.</p>

<p>"Well, perhaps your feelings may be different,"
said Alice; "all I know is, it would
feel very queer to <i>me</i>."</p>

<p>"You!" said the Caterpillar contemptuously.
"Who are <i>you?</i>"</p>

<p>Which brought them back again to the beginning
of the conversation. Alice felt a little
irritated at the Caterpillar's making such <i>very</i>
short remarks, and she drew herself up and
said, very gravely, "I think you ought to tell
me who <i>you</i> are, first."</p>

<p>"Why?" said the Caterpillar.</p>
`},
		{id: 3, content:`<p>Here was another puzzling question; and
as Alice could not think of any good reason,
and as the Caterpillar seemed to be in a
<i>very</i> unpleasant state of mind, she turned
away.</p>

<p>"Come back!" the Caterpillar called after
her. "I've something important to say!"</p>

<p>This sounded promising, certainly: Alice
turned and came back again.</p>

<p>"Keep your temper," said the Caterpillar.</p>

<p>"Is that all?" said Alice, swallowing down
her anger as well as she could.</p>

<p>"No," said the Caterpillar.</p>

<p>Alice thought she might as well wait, as
she had nothing else to do, and perhaps after
all it might tell her something worth hearing.
For some minutes it puffed away without
speaking, but at last it unfolded its arms,
took the hookah out of its mouth again, and
said, "So you think you're changed, do
you?"</p>

<p>"I'm afraid I am, sir," said Alice; "I can't
remember things as I used—and I don't keep
the same size for ten minutes together!"</p>

<p>"Can't remember <i>what</i> things?" said the
Caterpillar.</p>`}
	]
</script>

<svelte:head>
<title>Simple Pager Demo</title>
</svelte:head>

<Pager {contents}/>