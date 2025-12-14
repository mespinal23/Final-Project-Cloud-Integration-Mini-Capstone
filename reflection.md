# Reflection

##  <ins>Areas of Confidence</ins>

The part of this project I felt most confident about was defining the problem and explaining why it matters in a real clinical setting. Chemotherapy scheduling and chair utilization are challenges I see regularly, so turning those day-to-day issues into a use case felt very natural. The problem is not hypothetical for me; it directly affects patients, schedulers, and nursing staff. Because of that, it was easy to identify realistic data sources such as nurse staffing levels, scheduled chair time, and actual infusion duration, and to clearly explain how inaccuracies in these areas contribute to last-minute scheduling, unused capacity, and added stress for both staff and patients.

I was also comfortable mapping out the overall data flow and selecting cloud services that fit the needs of this problem. Thinking through how data would move from intake to storage, processing, and analysis felt intuitive, especially since we covered similar patterns throughout the course. Using serverless compute, cloud storage, and a managed database made sense not only from a technical standpoint but also from an operational and cost perspective. These choices reflect how healthcare organizations often approach cloud solutions: focusing on scalability, reliability, and minimizing overhead. Overall, this part of the project allowed me to connect course concepts directly to a real-world healthcare workflow that I already understand well.

## <ins>Areas of Uncertainty</ins>

The area I felt least confident about was how this design would perform at scale in a real clinical environment. While the proposed architecture works well for uploading files, processing data in batches, and generating summary reports, a live clinical setting would introduce additional complexity. In practice, scheduling decisions often change throughout the day due to cancellations, delays, or staffing adjustments, and a production system would need to handle real-time updates and much larger volumes of data. Designing for that level of complexity requires deeper integration with existing clinical systems and more advanced scheduling logic, which was beyond the scope of this assignment.

I was also less certain about how advanced the analytics component should be. For this project, I intentionally kept the analysis simple and focused on descriptive metrics, such as average chair utilization and differences between scheduled and actual infusion time. This approach felt appropriate for demonstrating core concepts without overcomplicating the solution. However, in a real-world environment, schedulers and managers would likely benefit from more advanced analytics, such as predictive models that estimate infusion duration or identify patients at higher risk for delays. Determining the right balance between simplicity and sophistication is something I would want to explore further in a future iteration.

## <ins>Alternative Architecture Considered</ins>

I considered using a traditional virtual machine to host the application and data processing logic. This approach would offer more direct control over the environment and might be familiar to some teams. However, it would also require more ongoing maintenance, including managing updates, security patches, and uptime. For this project, I ultimately chose a serverless approach because it reduces operational overhead, is easier to manage, and is more cost-effective for a student environment.

In addition, serverless services better reflect how many healthcare organizations are moving toward cloud adoption today. By using managed and serverless components, the focus stays on solving the operational problem rather than on infrastructure management, which aligned well with the goals of this assignment.

## <ins>Future Improvements</ins>

If I had additional time and access to more cloud resources, I would expand this system to support more proactive scheduling and planning. One major improvement would be the inclusion of predictive chair-time estimates based on historical infusion patterns, treatment regimens, and real-time nurse staffing levels. This could help schedulers make more accurate decisions earlier in the scheduling process and reduce last-minute changes.

I would also explore tighter integration with existing scheduling systems or electronic health record (EHR) platforms, allowing data to flow automatically rather than relying on manual uploads. Finally, I would create role-specific dashboards tailored to different users, such as schedulers and nurse managers, so each group could easily access the information most relevant to their responsibilities. Together, these enhancements would support better planning, improve efficiency, and help reduce the scheduling challenges that motivated this project in the first place.

