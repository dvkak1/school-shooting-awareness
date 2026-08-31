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
 		description: "According to the surviving court record, student Pablito Daffon fired a gun inside the auditorium, fatally striking 17-year-old graduating Alfredo Amadora.",
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
 ];
</script>