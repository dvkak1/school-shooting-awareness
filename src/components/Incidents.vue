<template>
	<section class="py-5" id="incident-overview">
		<div class="container py-4">
			
			<p class="eyebrow text-center">DOCUMENTED INCIDENTS</p>

			<h2 class="text-center mb-3">
				A Timeline of School-Related Firearm Incidents
			</h2>

			<p class="lead text-center mx-auto mb-5" style="max-width: 800px;">
				This timeline examines documented firearm-related incidents connected to Philippine educational institutions. It is not intended to represent the complete history of school violence in the Philippines. Each incident is presented according to what available sources establish.
			</p>

			<div class="row justify-content-center g-4">
              <div
              v-for ="incident in incidents"
              :key="incident.id" 
              class="col-lg-9">
              	<IncidentCard 
              	   :date="incident.date"
              	   :title="incident.title"
              	   :location="incident.location"
              	   :classification="incident.classification"
              	   :status="incident.status"
              	   :description="incident.description"
              	   :context="incident.context"
              	/>
              </div>
			</div>
		</div>
 </section>
</template>

<script setup>
 import IncidentCard from "./IncidentCard.vue" 

 const incidents = [
 	{
 		id: 1,
 		date: "April 13, 1972",
 		title: "The Amadora Shooting",
 		location: "Colegio de San Jose-Recoletos, Cebu",
 		classification: "School shooting - single fatality",
 		status: "Limited historical record",
 		description: "On April 13, 1972, 17 year old graduating student Alfredo Amadora was fatally shot inside the auditorium of Colegio de San Jose-Recoletos by his classmate, Pablito Daffon.",
 		context: "The incident later became the subject of Amadora v. Court of Appeals before the Philippine Supreme Court."
 	},
 	{
 		id: 2,
 		date: "March 24, 2014",
 		title: "The Claveria Incident",
 		location: "Rizal National High School, Claveria",
 		classification: "School shooting - single fatality",
 		status: "Limited historical record",
 		description: "Nineteen-year-old student Jundry Balayong was shot inside a classroom at Rizal National High School in Claveria and later died from his injuries",
 		context: "The incident was reported by SunStar as a shooting involving fellow student Nico Labastida. The available report provides limited information about the circumstances surrounding the incident."
 	},
 	{
 		id: 3,
 		date: "July 4, 2019",
 		title: "Calamba School Shooting",
 		location: "Castor Alviar National High School, Calamba, Laguna",
 		classification: "School shooting - single fatality",
 		status: "Multiple contemporary reports",
 		description: "Mark Anthony Miranda, 15 year old Grade 7 student, was shot twice inside his classroom at Castor Alviar National High School in Barangay Masili, Calamba City. He was taken to a hospital and died later that afternoon.",
 		context: "Initial police reports identified Renz Ivan Valderama as the suspect. Investigators said the suspect had reported been in a relationship with Miranda and that his motive has not yet been determined at the time of the initial investigation."
 	},
 	{
 		id: 4,
 		date: "July 24, 2022",
 		title: "Ateneo De Manila University Shooting",
 		location: "Ateneo De Manila University, Quezon City",
 		classification: "University mass shooting - three fatalities",
 		status: "Extensively reported",
 		description: "A gunman opened fire at Ateneo De Manila University as the Ateneo Law School's graduation ceremony was about to begin. Former Lamitan mayor Rose Furigay, her aide Victor Capistramo, and university security guard Jeneven Bandiala were killed.",
 		context: "Furigay's daughter Hannah, a graduating Law school student, was also wounded. Police said the suspect had a personal dispute with Furigay, making the attack distinct from a random attack against the university community."
 	},
 	{
 		id: 5,
 		date: "November 13, 2022",
 		title: "The Tugegarao University Shooting",
 		location: "St. Paul University Philippines, Tugegarao City",
 		classification: "University shooting - targeted attack",
 		status: "Multiple contemporary reports",
 		description: "A third-year medical technology student was assaulted and shot by a male classmate in the parking area of St. Paul University Philippines. The victim survived the attack.",
 		context: "Police investigated the incident as a targeted attack involving two people who knew each other. Reports connected the shooting to the suspect's romantic interest in the victim and her rejection of his advances.",
 	},
 	{
 		id: 6,
 		date: "August 4, 2025",
 		title: "The Lanao Del Sur School Shooting",
 		location: "Lanao del Sur",
 		classification: "School shooting - single fatality",
 		status: "Multiple contemporary reports",
 		description: "A Grade 11 student shot and killed his teacher inside a school in Lanao del Sur following a dispute over a failing grade.",
 		context: "The incident was treated as a targeted attack against the teacher. Authorities investigated the circumstances surrounding the shooting and the student's access to the firearm",
 	},
 	{
 		id: 7,
 		date: "August 7, 2025",
 		title: "The Santa Rosa School Shooting",
 		location: "Santa Rosa Integrated School, Santa Rosa, Nueva Ecija",
 		classification: "School shooting - targeted attack",
 		status: "Multiple contemporary reports",
 		description: "An 18-year-old former student entered Santa Rosa Integrated School and shot a 15-year-old student inside her classroom. He then turned the firearm on himself. Both were hospitalized, but the suspect died the following day and the student died five days after the shooting.",
 		context: "The incident drew attention to school security and the safety of students outside major urban centers. Authorities also investigated how the firearm was obtained and provided crisis intervention and psychosocial support and school personnel.",
 	},
 	{
 		id: 8,
 		date: "June 22, 2026",
 		title: "Tacloban School Shooting",
 		location: "San Jose National High School, Tacloban City",
 		classification: "Mass school shooting - three fatalities",
 		status: "Extensively documented",
 		description: "On June 22, 2026, a shooting inside San Jose National High School left three students dead and many others injured. Two minor suspects were later taken into custody.",
 		context: "Police later said the attack had allegedly been planned for more than a month, The incident prompted heightened security measures in Tacloban schools and a broader investigation into school safety."

 	},
 	{
 		id: 9,
 		date: "August 18, 2026",
 		title: "Zamboanga School Shooting",
 		location: "Ateneo de Zamboanga University, Zamboanga City",
 		classification: "School shooting - one student fatality",
 		status: "Extensively documented",
 		description: "On August 18, 2026, a Grade 9 student entered the Ateneo de Zamboanga school campus with firearms and opened fire, killing a Grade 10 student before dying by suicide.",
 		context: "The incident occured less than two months after the Tacloban shooting and led to another national discussion about school security and the access of students to firearms",
 	}
 ];
</script>