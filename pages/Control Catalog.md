---
title: Control Catalog
permalink: /control-catalog/
variant: markdown
description: ""
---
## Purpose

Within the OSCAL framework, a **catalog** represents a collection of **controls**. The catalog model is designed to represent security and privacy controls in standardised, machine-readable formats.

These controls are catagorised into **profiles** that represent security baselines and selected for implementation in **system security plans**. As different system security plans have different selections of controls depending on the type and sensitivity of the systems covered, not all controls will be in use at any one time.

The IM8-lite catalog serves as a central pool of controls.

<style>
	
	#grid.controls {
	  display: grid;
	  grid-template-columns: repeat(4, minmax(0, 1fr));
	  grid-auto-rows: 1fr;
	  grid-gap: 30px;
	}
	#grid.controls > div.content {
	  display: contents;
  }
	
	#grid.controls > div.content a {
	  border: 1px solid #d6d6d6;
	  border-radius: 8px;
	  padding: 16px;
    display: flex;
	  justify-content: center;
	  align-items: center;
	  text-align: center;
	  height: 100%;
    text-decoration: none;
	  font-weight: bold;
	}
	</style>
	
<p></p><h3 class="controls-title">Control Catalog</h3><p></p>
<div class="controls" id="grid">
	<div class="content">
	  <div><a href="/control-catalog/as/" rel="noopener noreferrer nofollow">Application Security</a></div>
		<div><a href="/control-catalog/sc/" rel="noopener noreferrer nofollow">Software Supply Chain</a></div>
		<div><a href="/control-catalog/st/" rel="noopener noreferrer nofollow">Security Testing</a></div>
		<div><a href="/control-catalog/ns/" rel="noopener noreferrer nofollow">Network Security</a></div>
	</div>
	<div class="content">
		<div><a href="/control-catalog/br/" rel="noopener noreferrer nofollow">Backup and Recovery</a></div>
		<div><a href="/control-catalog/dp/" rel="noopener noreferrer nofollow">Data Protection</a></div>
		<div><a href="/control-catalog/lm/" rel="noopener noreferrer nofollow">Logging and Monitoring</a></div>
		<div><a href="/control-catalog/ac/" rel="noopener noreferrer nofollow">Access Control</a></div>
	</div>
	<div class="content">
		<div><a href="/control-catalog/cs/" rel="noopener noreferrer nofollow">Container Security</a></div>
	  <div><a href="/control-catalog/pm/" rel="noopener noreferrer nofollow">Security Programme Management</a></div>
	  <div><a href="/control-catalog/is/" rel="noopener noreferrer nofollow">Infrastructure Security</a></div>
	  <div><a href="/control-catalog/sd/" rel="noopener noreferrer nofollow">Secure Development</a></div>
	</div>
	<div class="content">
	  <div><a href="/control-catalog/dc/" rel="noopener noreferrer nofollow">Datacentre</a></div>
	</div>
</div>