<script>
	import { page } from '$app/stores';

	const posts = {
		'aesthetics': {
			title: 'I was wrong about aesthetics',
			date: '2025-03-16',
			content: `
          	<p>
				Aesthetics, such a complementary thing in life. Life is about essentials and important things. When it comes to clothes, I used to think you should wear simple, good-quality ones in black or brown. Dark blue felt like a stretch, and mixing in flashy colors like red? Absolutely forbidden. With food, I believed in eating healthy. What people call a "treat meal" isn’t a treat—it’s a cheat meal. In coding, I obsessed over performance. I’d squeeze every bit of speed out of the code, even if it turned ugly. That was fine, because it was fast—blazingly fast. And don’t get me started on code editors. Those theme-obsessed hippies, asking their favorite YouTuber, "Oh, what’s the name of that beautiful theme?" Khukh. Some even buy fonts. No comment needed.
			</p>
			<p>
				That’s how I used to approach everything—always picking simple, sensible defaults and trusting people smarter than me who followed frameworks and best practices. How did I feel about it? It didn’t matter! I figured I didn’t know better and would get used to it. But then I read an article by David Heinemeier Hansson that shook me. He wrote about how much he enjoys writing Ruby, despite its obvious performance trade-offs, and how that joy matters. It made me question the rigid framework I’d trapped myself in.
			</p>
			<p>
				Recently, I also heard Mitchell Hashimoto, the creator of the Ghostty terminal, on a podcast. He was asked why he chose the Zig programming language over Rust or Go—a language he’d mastered over a decade. His answer? "I don’t enjoy writing Go anymore." Instead, he found joy in Zig. That hit me hard. We—you, me, all of us—spend so much time at our computers. Why torture ourselves with what the gurus say is the "right" way? Why not choose what we enjoy?
			</p>
          	<p>
				Hansson and Hashimoto made it clear: enjoyment isn’t a luxury—it’s essential, especially in things we do every day, like coding. It’s not just about best practices or peak performance; it’s about finding joy in the process. So, I was wrong about aesthetics. They’re not just complementary—they’re vital. Why not choose what makes you happy?
			</p>
        	`
		},
		'learning-and-touch-typing': {
			title: 'Learning and Touch Typing',
			date: '2025-05-18',
			content: `
				<p>
					We generally know a lot about learning—how to learn effectively and what hinders the learning process. Yet sometimes, or quite often, we tend to do things that impede our progress or make learning sessions pointless. We can continue this way for a long time without much reflection, but eventually, it will haunt us when we discover our "efforts" went in vain. This realization manifests in different ways: most notably as bad grades if you're taking an exam, but much learning happens outside school (I believe). Whether we're learning for work, a project, shifting careers and exploring a new domain, or mastering something personally important like another language, we often lack formal evaluation. Nevertheless, the consequences of ineffective learning will eventually surface one way or another.
				</p>
				<p>
					One frustrating experience I've had is when you Google or ask an AI about a problem, and the result looks strangely familiar—like déjà vu. It seems familiar because you think you know this information, but you don't. This happens repeatedly until you finally realize you've searched for this before, but somehow it didn't stick.
				</p>
				<p>
					The reality is that the information didn't stick because the learning process itself wasn't efficient enough. Perhaps we weren't concentrating adequately, or we failed to review the information properly. The concentration issue can involve many factors: multitasking (like listening to something while reading), being stressed, or feeling tired.
				</p>
				<p>
					It's challenging to keep these principles in mind whenever we're learning something new so we can make appropriate adjustments. I think this difficulty stems from how hard it is to benchmark the learning process in the short term. If we had a graph or signals moving up and down while learning, we could instantly adjust our approach or at least pause to identify what's wrong.
				</p>
				<p>
					That said, some skills we learn can be benchmarked, and touch typing is one of those things.
				</p>
				<p>
					Learning to touch type for the first time or changing from a familiar keyboard layout can be incredibly daunting—so much so that you might want to give up and continue hunt-and-peck typing or stick with your current layout. I've experienced both scenarios.
				</p>
				<p>
					I first learned touch typing on an AZERTY layout, which was painful. It was equally challenging when I later switched to Dvorak, making me want to revert to AZERTY. I felt the same way about a year ago when I decided to learn QWERTY, mainly because default shortcuts in most software are designed with QWERTY in mind.
				</p>
				<p>
					This urge to give up appears in almost any type of learning, whether it's a physical activity like driving or an intellectual pursuit like mastering specific software or learning a new language—be it natural or programming.
				</p>
				<p>
					Learning can be fun and relatively easy at the beginning. For example, when learning to drive, you can quickly understand what the steering wheel, gear stick, gas pedal, brake pedal, and clutch pedal do. However, coordinating all these elements while also checking the rearview mirror periodically is far from simple. Touch typing follows the same pattern: the concepts are straightforward, but placing all fingers correctly on the home row and moving only the appropriate fingers to type specific letters is much more challenging. The difference is that touch typing is easily benchmarked with measurements of accuracy, typing speed, and immediate feedback when you type incorrect letters.
				</p>
				<p>
					This observable aspect of learning reveals much more. For instance, when you attempt to multitask by typing while listening to something, you'll notice how significantly it affects your speed, accuracy, or both. Beyond multitasking, factors like fatigue, stress, rushing, or lack of focus can all impair your typing performance.
				</p>
				<p>
					While these observations might seem obvious, we need to remember them whenever we're learning something that can't be easily measured. We should pause and consider whether we're approaching the task correctly or at an appropriate time. We can compare our experience to touch typing or any other easily benchmarked skill that resonates with our personal experience.
				</p>
			`
		}
	};

	let post = $derived(posts[$page.params.slug]);
</script>

<article class="mx-auto max-w-2xl">
	{#if post}
		<header class="mb-8">
			<h1 class="text-3xl font-semibold text-white">{post.title}</h1>
			<time class="mt-2 block text-gray-400">
				{new Date(post.date).toLocaleDateString('en-US', {
					year: 'numeric',
					month: 'long',
					day: 'numeric'
				})}
			</time>
		</header>

		<div class="prose">
			{@html post.content}
		</div>

		<div class="mt-16">
			<a href="/blog" class="text-blue-400 hover:text-blue-300">← All posts</a>
		</div>
	{:else}
		<div class="py-12 text-center">
			<h1 class="mb-4 text-2xl font-semibold text-white">Post not found</h1>
			<a href="/blog" class="text-blue-400 hover:text-blue-300">Back to blog</a>
		</div>
	{/if}
</article>
