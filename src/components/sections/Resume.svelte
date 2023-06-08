<script>
	import {
		Accordion,
		AccordionContent,
		AccordionItem,
		AccordionTrigger
	} from '$components/ui/accordion';
</script>

<Accordion type="single" collapsible class="w-full p-4">
	<AccordionItem value="item-1">
		<AccordionTrigger class="text-4xl text-bold">Education</AccordionTrigger>
		<AccordionContent class="m-4 text-base">
			<div class="text-2xl font-black">Salisbury University</div>
			<br />
			<div>Bachelor of Science in Computer Science</div>
			<br />
			<div>Computational Data Science Minor</div>
			<div>Computational Mathematical Science Minor</div>
			<br />
			<div>Expected December 2023</div>
		</AccordionContent>
	</AccordionItem>
	<AccordionItem value="item-2">
		<AccordionTrigger class="text-4xl text-bold">Experience</AccordionTrigger>
		<AccordionContent class="m-4 text-base">
			<div class="text-2xl font-black">Software Engineer Contractor</div>
			<div>
				<a class="text-blue-500 underline" href="https://www.flikshop.com/" target="”_blank”"
					>Flikshop</a
				> | Washington, DC
			</div>
			<div>August 2022 - May 2023</div>
			<br />
			<div>
				<div>
					• Spearheaded the development of a front-end Learning Management System (LMS) in an
					Android environment using Kotlin.
				</div>
				<br />
				<div>
					• Collaborated with an agile team to prioritize and scope feature requests, ensuring that
					high-impact features were given top priority.
				</div>
				<br />
				<div>
					• Contributed to the successful completion of the project by delivering high-quality code,
					actively participating in code reviews, and identifying and resolving issues promptly.
				</div>
			</div>
			<br />
			<div class="text-2xl font-black">Research Fellow</div>
			<div>Salisbury University | Salisbury, MD</div>
			<div>MAy 2022 - September 2023</div>
			<br />
			<div>
				<div>
					• Conducted research on ”Exploiting Geometry in Robust Signal Processing and Feature
					Extraction.”
				</div>
				<br />
				<div>
					• Applied advanced techniques in tensor decomposition to learn latent variables in
					high-dimensional Gaussian Mixture Models, resulting in more robust signal processing and
					feature extraction.
				</div>
			</div>
		</AccordionContent>
	</AccordionItem>
	<AccordionItem value="item-3">
		<AccordionTrigger class="text-4xl text-bold">Community</AccordionTrigger>
		<AccordionContent class="m-4 text-base">
			<div class="text-2xl font-black">President</div>
			<div>Math, Computer Science and Data Science Club</div>
			<div>Salisbury University | Salisbury, MD</div>
			<div>August 2022 - Present</div>
			<br />
			<div>
				• Managed a team of officers to ensure the smooth functioning of the club and effective
				collaboration between members.
			</div>
			<br />
			<div>
				• Organized and led weekly meetings to discuss current topics in mathematics, computer
				science, and data science and to provide a platform for members to present their projects
				and research.
			</div>
			<br />
			<div class="text-2xl font-black">Math and Computer Science Tutor</div>
			<div>Salisbury University | Salisbury, MD</div>
			<div>August 2022 - Present</div>
			<br />
			<div>
				• Provided academic support to undergraduate students in the Math Emporium, demonstrating
				strong math skills.
			</div>
			<br />
			<div>
				• Effectively communicated complex concepts to students, resulting in improved academic
				performance.
			</div>
			<br />
			<div class="text-2xl font-black">Henson Student Leadership Advisory Council (HSLAC)</div>
			<div>Salisbury University | Salisbury, MD</div>
			<div>February 2022 - Present</div>
			<br />
			<div>• Henson School of Science: Comp. Science Representative</div>
			<br />
			<div>
				• Advocated for the concerns and ideas of computer science students to faculty and
				decision-making bodies.
			</div>
			<br />
			<div>
				• Organized workshops, conferences, and networking events to promote engagement and
				professional development.
			</div>
			<br />
			<div>
				• Mentored and supported fellow computer science students, providing guidance on academic
				and career-related matters.
			</div>
		</AccordionContent>
	</AccordionItem>
</Accordion>
