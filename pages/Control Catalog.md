---
title: Control Catalog
permalink: /control-catalog/
variant: markdown
description: ""
---
<style>
	#grid.controls {
	  display: grid;
	  grid-template-columns: repeat(4, minmax(0, 1fr));
	  grid-auto-rows: 1fr;
	  grid-gap: 15px;
	}
	
	#grid.controls > div.content {
	  display: contents;
  }
	
	#grid.controls > div.content a {
	  border: 1px solid #d6d6d6;
	  border-radius: 8px;
	  padding: 8px;
    display: flex;
	  justify-content: center;
	  align-items: center;
	  text-align: center;
	  height: 100%;
    text-decoration: none;
	}
	</style>

## Purpose

Within the OSCAL framework, a **catalog** represents a collection of **controls**. The catalog model is designed to represent security and privacy controls in standardised, machine-readable formats.

These controls are catagorised into **profiles** that represent security baselines and selected for implementation in **system security plans**. As different system security plans have different selections of controls depending on the type and sensitivity of the systems covered, not all controls will be in use at any one time.

The IM8-lite catalog serves as a central pool of controls.

<div class="controls" id="grid">
	<div class="content">
	  <div><a href="/control-catalog/001-application-security/" rel="noopener noreferrer nofollow">Application Security</a></div>
		<div><a href="/control-catalog/002-software-supply-chain/" rel="noopener noreferrer nofollow">Software Supply Chain</a></div>
		<div><a href="/control-catalog/003-security-testing/" rel="noopener noreferrer nofollow">Security Testing</a></div>
		<div><a href="/control-catalog/004-network-security/" rel="noopener noreferrer nofollow">Network Security</a></div>
	</div>
	<div class="content">
		<div><a href="/control-catalog/005-backup-and-recovery/" rel="noopener noreferrer nofollow">Backup and Recovery</a></div>
		<div><a href="/control-catalog/006-data-protection/" rel="noopener noreferrer nofollow">Data Protection</a></div>
		<div><a href="/control-catalog/007-logging-and-monitoring/" rel="noopener noreferrer nofollow">Logging and Monitoring</a></div>
		<div><a href="/control-catalog/008-access-control/" rel="noopener noreferrer nofollow">Access Control</a></div>
	</div>
	<div class="content">
		<div><a href="/control-catalog/009-container-security/" rel="noopener noreferrer nofollow">Container Security</a></div>
	  <div><a href="/control-catalog/010-security-programme-management/" rel="noopener noreferrer nofollow">Security Programme Management</a></div>
	  <div><a href="/control-catalog/011-infrastructure-security/" rel="noopener noreferrer nofollow">Infrastructure Security</a></div>
	  <div><a href="/control-catalog/012-secure-development/" rel="noopener noreferrer nofollow">Secure Development</a></div>
	</div>
	<div class="content">
	  <div><a href="/control-catalog/013-datacentre/" rel="noopener noreferrer nofollow">Datacentre</a></div>
	</div>
</div>

| Control Catalog | | | |
| -- | -- | -- | -- |
| [Application Security](/control-catalog/001-application-security/) | [Software Supply Chain](/control-catalog/002-software-supply-chain/) | [Security Testing](/control-catalog/003-security-testing/) | [Network Security](/control-catalog/004-network-security/) |
| [Backup and Recovery](/control-catalog/005-backup-and-recovery/) |  [Data Protection](/control-catalog/006-data-protection/) | [Logging and Monitoring](/control-catalog/007-logging-and-monitoring/) | [Access Control](/control-catalog/008-access-control/) | 
[Container Security](/control-catalog/009-container-security/) | [Security Programme Management](/control-catalog/010-security-programme-management/) | [Infrastructure Security](/control-catalog/011-infrastructure-security/) | [Secure Development](/control-catalog/012-secure-development/) | 
[Datacentre](/control-catalog/013-datacentre/) |