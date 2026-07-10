---
title: "Event 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# FCAJ Community Day Report: Data Driven, AI Risen

### Event Objectives

The **FCAJ Community Day "Data Driven, AI Risen"** event gave me a practical view of how Data, AI, Cloud, and Agentic AI are being applied in enterprise environments. The content was not only about AI for content generation or coding assistance, but also covered more complex problems such as cloud operations, incident handling, voice agents, HR process optimization, and secure connections to internal systems.

Through the sessions, I understood that AI is gradually becoming an important part of enterprise operations. However, to apply AI effectively, a system still needs good data, suitable architecture, risk control mechanisms, and human supervision.

### Speakers

- **Steve Tran** - Founder of CloudThinker - Topic: AgenticOps for Your Cloud
- **Nghi Danh, Trung Vu, Kiet Tran** - Topic: Building Voice Agent at Scale
- **Nguyen Nguyen, Bao Phan** - Topic: AWS DevOps Agent: Your Always-Available Operation Teammate
- **Truong Tran, Anh Dang** - Topic: AI-Powered Productivity Workforce Planning for Enterprise
- **Toan Nguyen, Nghi Danh** - Topic: Building Secure Private MCP for Quick

### Key Highlights

#### AgenticOps for Your Cloud

Steve Tran's session helped me understand more about the journey of developing in the cloud field and the challenges of operating cloud infrastructure in enterprises. The speaker shared his learning process, AWS journey, certification experience, cloud work, and how CloudThinker was developed to solve complex operation problems.

One point I learned is that cloud is not simply a place to deploy applications. When companies move from traditional servers or on-premise systems to the cloud, the system can scale more flexibly but also creates new challenges such as monitoring, security, cost, incidents, and technical debt. When a system grows into many microservices, tracking logs, metrics, alerts, and dependencies between services becomes much more difficult.

CloudThinker was introduced as an **AgenticOps** platform that supports cloud operations using AI agents. Its capabilities include incident investigation, pull request review, cloud cost optimization, security issue analysis, and debugging support. I understand AgenticOps as an approach where AI does not only answer questions but also participates in operational workflows step by step: collecting data, analyzing context, suggesting solutions, and supporting human decision-making.

This session also gave me a clearer view of the job market in the AI era. AI can strongly support code generation, but jobs related to production systems, cloud operations, security, observability, and incident handling still require experienced people to control risks and make suitable decisions.

#### Building Voice Agent at Scale

The session by Nghi Danh, Trung Vu, and Kiet Tran focused on building voice agents at scale. This helped me understand the basic architecture of a voice AI system and the challenges of moving a system from demo to production.

A voice agent usually has three main components: **Speech-to-Text (STT)** to convert speech into text, **Large Language Model (LLM)** to understand the request and generate a response, and **Text-to-Speech (TTS)** to convert the response into voice output. The basic flow is that the user speaks to the system, the audio is converted into text, the LLM processes the context, and the answer is converted back into voice.

An important point is that Vietnamese voice AI still has many opportunities. Vietnamese has specific characteristics such as tones, regional accents, pronouns, and communication context, so building a high-quality voice agent is not simple. This can be a good direction for students or research teams when building projects, joining competitions, or creating a portfolio.

I also realized the big difference between a demo and a production system. A demo may only need to listen and answer, but a real product must handle latency, streaming, output control, context understanding, action-taking, and human-in-the-loop. Especially in fields such as banking or customer support, AI must not only respond quickly but also respond correctly, safely, and according to business rules.

#### AWS DevOps Agent: Your Always-Available Operation Teammate

Nguyen Nguyen and Bao Phan introduced the DevOps Agent model as an always-available operation teammate for technical teams. In practice, when a system has an incident, engineers often need to check many data sources such as logs, metrics, alerts, dashboards, cloud configurations, and change history. Manual investigation takes time and can miss important signals.

DevOps Agent was presented as an AI agent that supports operations through three main stages: **Investigation**, **Mitigation**, and **Prevention**. In the investigation stage, the agent collects data and analyzes logs, metrics, or alerts to identify the affected area. In the mitigation stage, it suggests steps to reduce the impact of the incident. In the prevention stage, it summarizes lessons learned and suggests improvements to prevent similar incidents.

The difference between DevOps Agent and traditional monitoring tools is that the agent does not only display data. It also tries to understand system context, connect signals, and provide root causes or key findings. However, I also learned that in production environments, automated actions must be carefully controlled to avoid risks when AI decisions are not reliable enough.

#### AI-Powered Productivity Workforce Planning for Enterprise

The session by Truong Tran and Anh Dang expanded my view of AI into Human Resources. In the AI era, HR should not only handle resumes and recruitment manually, but also make decisions based on data. When the number of CVs is large, manual screening can take a lot of time, miss suitable candidates, and make the recruitment process less efficient.

Amazon Quick was introduced as an AI tool that supports data analysis, report generation, candidate filtering by skills or experience, and workforce planning. In a recruitment scenario, AI can read many CVs, summarize candidate information, and provide a more suitable shortlist for HR to review.

The important point is that AI does not completely replace HR. AI reduces repetitive work and supports data analysis, while humans still interview, evaluate, and make final decisions. This shows that AI can bring value to many departments, not only developers or technical teams.

#### Building Secure Private MCP for Quick

The session by Toan Nguyen and Nghi Danh focused on building a **Private MCP Server** to connect with Amazon Quick in a more secure environment. This was a highly technical topic related to networking, security, and cloud architecture.

Normally, for an AI assistant to connect to an MCP server, the system may need a public endpoint. However, public endpoints create risks such as internet scanning, DDoS attacks, Man-in-the-Middle risks, and possible exposure of internal data if access control is not strict.

The proposed solution is to place the MCP Server in a private subnet and allow Amazon Quick to connect through a **VPC Connection**. The general architecture can be understood as Amazon Quick sending requests through VPC Connection, the request entering the private network through an ENI, then going to an Internal ALB and the MCP Server in a private subnet. The MCP Server can query internal tools such as Jaeger or private data sources and return results to the user.

This session helped me understand how to bring AI into enterprise systems while still maintaining security. When an AI assistant needs to access internal tools or data, companies should avoid exposing public endpoints when possible and should prioritize private networking, VPC, access control, and data protection.

### What I Learned

#### About AgenticOps And Cloud Operations

- Cloud operations is important because production systems are becoming more complex.
- When a system has many microservices, logs, metrics, alerts, security, and cost become harder to control.
- AgenticOps can support engineers in incident handling, change review, cost optimization, and security issue detection.
- AI cannot fully replace production operation teams because humans still need to evaluate context and control risk.

#### About Voice Agents

- A voice agent has a basic architecture of STT, LLM, and TTS.
- Vietnamese voice AI still has many opportunities for development.
- Production voice agents need to consider latency, streaming, output control, context, and human-in-the-loop.
- In sensitive fields such as banking, AI needs clear role limits and careful response control.

#### About DevOps Agent

- Manual incident investigation takes time because data is spread across many tools.
- DevOps Agent can support investigation, mitigation, and prevention.
- AI agents can summarize logs, metrics, alerts, and change history to provide root causes or key findings.
- Automated actions in production need control mechanisms to ensure safety.

#### About AI In HR

- HR in the AI era should move from manual processing to data-driven decision-making.
- AI can support CV analysis, report generation, candidate filtering, and workforce planning.
- AI improves productivity, but humans still make the final evaluation.

#### About Private MCP And Security

- MCP helps AI assistants connect to external tools and data.
- Public MCP endpoints can create many security risks for enterprise systems.
- VPC Connection and private subnets help connect AI with internal systems more safely.
- When integrating AI into enterprise systems, security and access control are very important.

### Applying The Lessons To Myself

After the event, I realized that when learning cloud, I should not only focus on deploying applications. I also need to learn more about cloud operations, SRE, observability, incident response, security, and cost optimization. These topics help me better understand how production systems are operated in enterprises.

For AI projects, I need to pay more attention to domain knowledge, data, model limitations, and output control. If I study voice agents, I can start with the basic architecture of STT, LLM, and TTS, then gradually expand to latency, streaming, and human-in-the-loop. In addition, when building systems connected to internal data, I should prioritize security, private networking, and access control from the beginning.

### Event Experience

Attending FCAJ Community Day **"Data Driven, AI Risen"** gave me many new and practical insights. The event helped me see that AI is not only a tool for studying or coding assistance, but is also being applied more deeply in enterprise activities such as cloud operations, DevOps, HR analytics, voice agents, and internal system security.

The AgenticOps session helped me understand that cloud operations is a complex and critical area. The voice agent session helped me imagine how voice AI works and why production deployment is much harder than a demo. The DevOps Agent session showed how AI can support incident investigation, while the HR session showed that AI can also bring value to non-technical departments.

Some topics such as MCP, ENI, Route 53 Resolver, Internal ALB, Jaeger, observability, and root cause analysis are still quite new to me, so I need to continue learning more. However, these difficult topics helped me realize that I need to study AWS networking, security, monitoring, and production systems more deeply if I want to keep up with AI trends in enterprises.

### Lessons Learned

- AI is being applied more deeply in cloud operations, DevOps, HR, voice agents, and system security.
- As cloud infrastructure grows, operations, monitoring, security, and cost optimization become more important.
- AgenticOps can support incident handling, code review, cost optimization, and security analysis.
- Production voice agents require more than demos, including latency, streaming, output control, and human-in-the-loop.
- DevOps Agent can reduce incident investigation time but still needs control mechanisms in production.
- AI in HR improves data processing productivity but does not fully replace humans.
- Private MCP is an important approach when connecting AI with internal enterprise systems.
- Students should continue learning cloud, security, observability, and production systems to prepare better for future work.

### Conclusion

Through FCAJ Community Day "Data Driven, AI Risen", I gained a practical view of how AI is changing many areas in enterprises, from cloud operations and incident handling to voice agents, HR, and internal system security. The event helped me understand that applying AI effectively does not only require knowing how to use a model, but also requires understanding data, system architecture, business domains, and risk control. I also realized that I need to proactively learn more about cloud operations, DevOps, security, observability, and AI agent models to build a stronger foundation for the future.
