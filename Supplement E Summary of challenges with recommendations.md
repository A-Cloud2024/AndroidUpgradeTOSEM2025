# Supplement E Summary of Challenges with Recommendations

During the research process, we observed the challenges and difficulties in the Android upgrade conflict scenarios, and summarized the actual pain points encountered by Android vendors in the different stages of the upgrade, details of which can be found in Chapters 5-8, and a list of the information can be seen in the overview table below.  

⭐star mark refers to the priority of challenges and recommends. 

The icon in front of each suggestion represents its type: 📆management, 📄documentation, 🛠️tools️, 🧑‍💻process. 
<table>
  	<tr>
		<td align="left" ><b>Stage</b></td>
		<td align="left" ><b>Challenge</b></td>
        	<td align="left" ><b>Recommend</b></td>
	</tr>
	<tr>
		<td align="left"  rowspan="4"><b>Baseline Analysis</b></td>
		<td align="left" >⭐<b>Architecture Compatibility.</b> The intricacies of AOSP's architectural changes encompass deprecated, irreversible, and duplicated features, posing a challenge for downstream architectures to adapt (O1.1)</td>
        	<td align="left" >⭐🛠️🧑‍💻<b>Architecture Change Detection.</b> Architecture change detection tools can be enhanced to locate deprecated features, irreversible features, duplicated features, etc., and further bridge high-level architecture changes with implementation-level code modifications (R1.2)</td>
	</tr>
        <tr>
		<td align="left" >⭐<b>Upgrade Strategy Decision.</b> It is challenging to determine the most suitable Android upgrade strategy, whether to adopt a forward, reverse, or merger upgrade (O1.3)</td>
        	<td align="left" >⭐📄<b>Architecture Evolution Documentation.</b> It is significant to maintain comprehensive documentation of the architecture including features, architecture design, and the evolution process for Android systems (R1.1).</td>
	</tr>
	<tr>
		<td align="left" >⭐<b>Project TQC Prediction.</b> Before initiating the Android upgrade operations, it is imperative to anticipate not only the extent of merge conflicts, but also the upgrade cycle, upgrade quality, and potential cost investment (O1.4)</td>
        	<td align="left" >⭐🛠️<b>TQC Prediction Modeling.</b> It is urgent to build a TQC prediction model based on historical data to ensure a manageable Android upgrade process (R1.3)</td>
	</tr>
	<tr>
		<td align="left" ><b>Intense Upgrade Cycle.</b> Facing intense competition from peers and rapid Android update cycles, developers are under pressure to quickly identify AOSP architectural and code changes (O1.2)</td>
        	<td align="left" ></td>
	</tr>
    <tr>
		<td align="left"  rowspan="4"><b>Conflict Reason</b></td>
		<td align="left" >⭐<b>AOSP Rapid Iteration.</b> Upstream AOSP's frequent feature iterations, code refactoring, and  updates made by Google trigger conflicts (O2.1)</td>
        	<td align="left" >⭐🛠️🧑‍💻<b>Understanding Architectural Coupling.</b> Developers  can employ tools to figure out the coupling between downstream Android and upstream AOSP (R2.3)</td>
	</tr>
    <tr>
		<td align="left" >⭐<b>Unhealthy Architecture Design.</b> Bad  architecture design and abstractions tightly couple downstream Android with the upstream AOSP code, leading to recurring conflicts (O2.3)</td>
        <td align="left" >⭐🧑‍💻<b>Downstream Architecture Enhancement.</b> Downstream Android architecture should improve its modular design (R2.4)</td>
	</tr>
    <tr>
		<td align="left" >⭐<b>Inadequate Version Control Management.</b> Improper version management and branch synchronization issues cause conflicts (O2.4)</td>
        <td align="left" >⭐🧑‍💻<b>Emphasizing Hotspot and Conflict Types.</b> Developers should pay attention to hotspot conflict code and key conflict types (R2.2)</td>
	</tr>
    <tr>
		<td align="left" ><b>Intrusive Modifications.</b> Downstream Android variants make intrusive modifications into upstream AOSP, which leads to frequent conflicts. Those intrusive modifications involve customized feature development, change rollbacks, and hotspot classes depended by multiple modules (O2.2)</td>
        <td align="left" >🛠️🧑‍💻<b>Identification and Standardization of Intrusive Modifications.</b> It is crucial to detect intrusive modifications and enforce code standards on such modifications (R2.1).</td>
	</tr>
    <tr>
		<td align="left"  rowspan="4"><b>Conflict Resolution</b></td>
		<td align="left" >⭐<b>Obstacles of Conflict Resolution.</b> Major factors impede effective conflict resolution, including the dependencies associated with conflicting code, the conflicts between old and new versions of downstream code, and the divergence between upstream and downstream changes (O3.3)</td>
        	<td align="left" >⭐📆📄<b>Conflict Knowledge Transfer.</b> The development team should learn from past experiences and patterns to create systematic knowledge for facilitating conflict resolution (R3.2)</td>
	</tr>
    <tr>
		<td align="left" ><b>Substantial Efforts on Conflict Analysis.</b> Analyzing the commit history of conflicting code is the most time-consuming in manual conflict resolution, followed by devising resolution solutions (O3.1)</td>
        	<td align="left" >📆📄<b>Resolution Guidelines and Team Collaboration.</b> It is advisable to establish conflict resolution guidelines and enhance team collaboration (R3.1)</td>
 	</tr>
    <tr>
		<td align="left" ><b>Change Intent Inspection.</b> Due to the unfamiliarity with upstream AOSP and downstream commits, developers find it challenging to pinpoint underlying change intent (O3.2)</td>
        	<td align="left" ></td>
	</tr>
    <tr>
        <td align="left" ><b>Insufficient Conflict Resolution Tools.</b> Developers utilize tools to improve conflict resolution efficiency but note deficiencies in accuracy, performance, and usability of tools (O3.4)</td>
        <td align="left" >🛠️<b>Merging Tool Improvement.</b> Existing merging tools can be improved for better accuracy, performance, and usability (R3.3)</td>
	</tr>
    <tr>
		<td align="left"  rowspan="4"><b>Conflict Impact</b></td>
        <td align="left" rowspan="2">⭐<b>Impact on Subsequent Workflow.</b> From the time perspective, improper conflict resolution will influence the subsequent phases during the Android update workflow, introducing semantic failures (O4.3)</td>
        <td align="left" >⭐📄🧑‍💻<b>Semantic Conflict Prediction.</b> Developers can summarize recurrent patterns to anticipate the conflict impact on semantic failures (R4.2)</td>
	</tr>
    <tr>
        <td align="left" >⭐🛠️🧑‍💻<b>Testing Modules On the Fly.</b> It can be considered to decouple architectural modules, enabling building and testing modules independently on the fly for an earlier exposure of semantic errors (R4.3)</td>
	</tr>
    <tr>
        <td align="left" ><b>Impact across Design Boundaries.</b> From the space perspective, conflicts across the design boundary influence both upstream and downstream code (O4.2)</td>
        <td></td>
	</tr>
    <tr>
        <td align="left" ><b>Impact Propagation via Dependencies.</b> From the code space perspective, conflict blocks often affect multiple files or even span across modules due to dependency propagation (O4.1)</td>
        <td align="left" >🧑‍💻<b>Conflict Dependency Analysis.</b> It is useful to evaluate conflict impact by employing dependency analysis to analyze related conflict blocks together (R4.1)</td>
	</tr>
</table>


