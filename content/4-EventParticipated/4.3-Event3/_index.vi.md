---
title: "Event 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

{{% notice note %}}
📌 **Info:** Báo cáo event tham gia về Data, AI, Cloud, AgenticOps, Voice Agent, DevOps Agent, AI trong HR và Secure Private MCP.
{{% /notice %}}

# Bài thu hoạch FCAJ Community Day: Data Driven, AI Risen

### Mục Đích Của Sự Kiện

Sự kiện **FCAJ Community Day "Data Driven, AI Risen"** giúp tôi có thêm góc nhìn thực tế về cách Data, AI, Cloud và Agentic AI đang được ứng dụng trong môi trường doanh nghiệp. Nội dung sự kiện không chỉ tập trung vào AI ở mức hỗ trợ tạo nội dung hoặc viết code, mà còn mở rộng sang các bài toán phức tạp hơn như vận hành hạ tầng cloud, xử lý incident, xây dựng voice agent, tối ưu quy trình HR và kết nối hệ thống nội bộ một cách an toàn.

Thông qua các phần trình bày, tôi hiểu rõ hơn rằng AI đang dần trở thành một phần quan trọng trong quá trình vận hành doanh nghiệp. Tuy nhiên, để ứng dụng AI hiệu quả, hệ thống vẫn cần có dữ liệu tốt, kiến trúc phù hợp, cơ chế kiểm soát rủi ro và vai trò giám sát của con người.

### Danh Sách Diễn Giả

- **Steve Tran** - Founder của CloudThinker - Chủ đề: AgenticOps for Your Cloud
- **Nghi Danh, Trung Vu, Kiet Tran** - Chủ đề: Building Voice Agent at Scale
- **Nguyen Nguyen, Bao Phan** - Chủ đề: AWS DevOps Agent: Your Always-Available Operation Teammate
- **Truong Tran, Anh Dang** - Chủ đề: AI-Powered Productivity Workforce Planning for Enterprise
- **Toan Nguyen, Nghi Danh** - Chủ đề: Building Secure Private MCP for Quick

### Nội Dung Nổi Bật

#### AgenticOps for Your Cloud

Phần chia sẻ của Steve Tran giúp tôi hiểu thêm về hành trình phát triển trong lĩnh vực cloud và những thách thức khi vận hành hạ tầng cloud trong doanh nghiệp. Diễn giả chia sẻ quá trình học tập, tiếp cận AWS, thi chứng chỉ, làm việc với cloud và sau đó phát triển CloudThinker để giải quyết các vấn đề vận hành phức tạp.

Một điểm tôi rút ra là cloud không chỉ đơn giản là nơi triển khai ứng dụng. Khi doanh nghiệp chuyển từ server truyền thống hoặc hệ thống on-premise lên cloud, hệ thống có thể mở rộng linh hoạt hơn nhưng cũng phát sinh nhiều vấn đề mới như monitoring, security, cost, incident và technical debt. Khi hệ thống phát triển thành nhiều microservices, việc theo dõi log, metric, alert và dependency giữa các service trở nên khó hơn rất nhiều.

CloudThinker được giới thiệu như một nền tảng **AgenticOps** hỗ trợ vận hành cloud bằng AI agents. Các khả năng chính bao gồm hỗ trợ điều tra sự cố, review pull request, tối ưu chi phí cloud, phân tích vấn đề bảo mật và hỗ trợ debug. Tôi hiểu AgenticOps là hướng tiếp cận trong đó AI không chỉ trả lời câu hỏi, mà còn tham gia vào quy trình vận hành theo từng bước: thu thập dữ liệu, phân tích bối cảnh, đề xuất phương án xử lý và hỗ trợ con người ra quyết định.

Phần này cũng giúp tôi có thêm góc nhìn về thị trường việc làm trong thời đại AI. AI có thể hỗ trợ rất mạnh trong việc viết code, nhưng các công việc liên quan đến production system, cloud operations, security, observability và xử lý sự cố vẫn cần con người có kinh nghiệm để kiểm soát rủi ro và đưa ra quyết định phù hợp.

#### Building Voice Agent at Scale

Phần trình bày của Nghi Danh, Trung Vu và Kiet Tran tập trung vào việc xây dựng voice agent ở quy mô lớn. Nội dung này giúp tôi hiểu rõ hơn kiến trúc cơ bản của một hệ thống AI giao tiếp bằng giọng nói và những thách thức khi đưa hệ thống từ demo lên production.

Một voice agent thường gồm ba thành phần chính: **Speech-to-Text (STT)** để chuyển giọng nói thành văn bản, **Large Language Model (LLM)** để hiểu yêu cầu và tạo phản hồi, và **Text-to-Speech (TTS)** để chuyển câu trả lời thành giọng nói. Luồng xử lý có thể hình dung là người dùng nói vào hệ thống, âm thanh được chuyển thành text, LLM xử lý ngữ cảnh và câu trả lời được chuyển lại thành voice output.

Điểm đáng chú ý là thị trường voice AI tiếng Việt vẫn còn nhiều cơ hội. Tiếng Việt có đặc thù về ngữ điệu, vùng miền, cách xưng hô và ngữ cảnh giao tiếp, nên việc xây dựng voice agent chất lượng cao không đơn giản. Đây có thể là hướng tốt cho sinh viên hoặc nhóm nghiên cứu khi muốn làm project, tham gia cuộc thi hoặc xây dựng portfolio.

Tôi cũng nhận ra sự khác biệt lớn giữa demo và production. Một demo có thể chỉ cần nghe và trả lời, nhưng sản phẩm thực tế cần giải quyết thêm nhiều vấn đề như latency, streaming, kiểm soát output, context understanding, action-taking và human-in-the-loop. Đặc biệt trong các lĩnh vực như ngân hàng hoặc chăm sóc khách hàng, AI không chỉ cần trả lời nhanh mà còn phải trả lời đúng, an toàn và phù hợp với nghiệp vụ.

#### AWS DevOps Agent: Your Always-Available Operation Teammate

Phần trình bày của Nguyen Nguyen và Bao Phan giới thiệu mô hình DevOps Agent như một "đồng đội vận hành" luôn sẵn sàng hỗ trợ đội ngũ kỹ thuật. Trong thực tế, khi hệ thống gặp incident, kỹ sư thường phải kiểm tra nhiều nguồn dữ liệu như log, metric, alert, dashboard, cấu hình cloud và lịch sử thay đổi. Việc điều tra thủ công như vậy tốn nhiều thời gian và dễ bỏ sót tín hiệu quan trọng.

DevOps Agent được trình bày như một AI agent có khả năng hỗ trợ quá trình vận hành qua ba giai đoạn chính: **Investigation**, **Mitigation** và **Prevention**. Ở giai đoạn investigation, agent thu thập dữ liệu và phân tích log, metric hoặc alert để xác định khu vực có vấn đề. Ở giai đoạn mitigation, agent đề xuất các bước giảm ảnh hưởng của sự cố. Sau đó, ở giai đoạn prevention, agent tổng hợp bài học và đề xuất cải thiện để tránh sự cố lặp lại.

Điểm khác biệt của DevOps Agent so với công cụ monitoring truyền thống là agent không chỉ hiển thị dữ liệu mà còn cố gắng hiểu bối cảnh hệ thống, liên kết các tín hiệu và đưa ra root cause hoặc key findings. Tuy nhiên, tôi cũng hiểu rằng trong môi trường production, các hành động tự động cần được kiểm soát cẩn thận để tránh rủi ro khi AI đưa ra quyết định chưa đủ chính xác.

#### AI-Powered Productivity Workforce Planning for Enterprise

Phần chia sẻ của Truong Tran và Anh Dang mở rộng góc nhìn của tôi về AI sang lĩnh vực Human Resources. Trong thời đại AI, HR không chỉ xử lý hồ sơ và tuyển dụng thủ công mà cần ra quyết định dựa trên dữ liệu. Khi số lượng CV quá lớn, việc đọc và lọc hồ sơ thủ công có thể tốn nhiều thời gian, dễ bỏ sót ứng viên phù hợp và khiến quy trình tuyển dụng thiếu hiệu quả.

Amazon Quick được giới thiệu như một công cụ AI hỗ trợ phân tích dữ liệu, tạo báo cáo, lọc ứng viên theo kỹ năng hoặc kinh nghiệm, và hỗ trợ workforce planning. Trong kịch bản tuyển dụng, AI có thể đọc số lượng lớn CV, tóm tắt thông tin ứng viên và đưa ra danh sách phù hợp để HR review tiếp.

Điểm tôi thấy quan trọng là AI không thay thế hoàn toàn HR. AI giúp giảm tải các công việc lặp lại và hỗ trợ phân tích dữ liệu, còn con người vẫn cần phỏng vấn, đánh giá và đưa ra quyết định cuối cùng. Điều này cho thấy AI có thể ứng dụng ở nhiều phòng ban khác nhau, không chỉ riêng developer hoặc đội ngũ kỹ thuật.

#### Building Secure Private MCP for Quick

Phần trình bày của Toan Nguyen và Nghi Danh tập trung vào cách xây dựng **Private MCP Server** để kết nối với Amazon Quick trong môi trường bảo mật hơn. Đây là phần có tính kỹ thuật cao, liên quan đến networking, security và cloud architecture.

Thông thường, để AI assistant kết nối đến MCP server, hệ thống có thể cần public endpoint. Tuy nhiên, public endpoint có nhiều rủi ro như bị scan từ internet, nguy cơ DDoS, rủi ro Man-in-the-Middle hoặc lộ dữ liệu nội bộ nếu kiểm soát truy cập chưa chặt.

Giải pháp được trình bày là đặt MCP Server trong private subnet và cho Amazon Quick kết nối thông qua **VPC Connection**. Kiến trúc tổng quát có thể hiểu là Amazon Quick gửi request qua VPC Connection, request đi vào private network thông qua ENI, sau đó đến Internal ALB và MCP Server trong private subnet. MCP Server có thể truy vấn các công cụ nội bộ như Jaeger hoặc các nguồn dữ liệu riêng rồi trả kết quả lại cho người dùng.

Tôi thấy phần này giúp hình dung rõ hơn cách đưa AI vào hệ thống enterprise mà vẫn đảm bảo bảo mật. Khi AI assistant cần truy cập công cụ hoặc dữ liệu nội bộ, doanh nghiệp không nên mở public endpoint nếu không cần thiết, mà nên ưu tiên private network, VPC, kiểm soát truy cập và cơ chế bảo vệ dữ liệu.

### Những Gì Tôi Học Được

#### Về AgenticOps Và Cloud Operations

- Cloud operations là một lĩnh vực quan trọng vì hệ thống production ngày càng phức tạp.
- Khi hệ thống có nhiều microservices, việc theo dõi log, metric, alert, security và cost trở nên khó kiểm soát hơn.
- AgenticOps có thể hỗ trợ kỹ sư trong việc xử lý incident, review thay đổi, tối ưu chi phí và phát hiện vấn đề bảo mật.
- AI khó thay thế hoàn toàn đội ngũ vận hành production vì vẫn cần con người đánh giá bối cảnh và kiểm soát rủi ro.

#### Về Voice Agent

- Voice agent có kiến trúc cơ bản gồm STT, LLM và TTS.
- Tiếng Việt vẫn còn nhiều cơ hội phát triển trong lĩnh vực voice AI.
- Voice agent production cần quan tâm đến latency, streaming, kiểm soát output, context và human-in-the-loop.
- Trong các lĩnh vực nhạy cảm như ngân hàng, AI cần được giới hạn vai trò và kiểm soát câu trả lời cẩn thận.

#### Về DevOps Agent

- Điều tra incident thủ công tốn nhiều thời gian vì dữ liệu nằm ở nhiều công cụ khác nhau.
- DevOps Agent có thể hỗ trợ investigation, mitigation và prevention.
- AI agent có thể tổng hợp log, metric, alert và lịch sử thay đổi để đưa ra root cause hoặc key findings.
- Các hành động tự động trong production cần có cơ chế kiểm soát để đảm bảo an toàn.

#### Về AI Trong HR

- HR trong kỷ nguyên AI cần chuyển từ xử lý thủ công sang ra quyết định dựa trên dữ liệu.
- AI có thể hỗ trợ phân tích CV, tạo report, lọc ứng viên và lập kế hoạch nhân sự.
- AI giúp tăng năng suất nhưng con người vẫn giữ vai trò đánh giá cuối cùng.

#### Về Private MCP Và Bảo Mật

- MCP giúp AI assistant kết nối với công cụ và dữ liệu bên ngoài.
- Public MCP endpoint có thể tạo ra nhiều rủi ro bảo mật cho hệ thống doanh nghiệp.
- VPC Connection và private subnet giúp kết nối AI với hệ thống nội bộ an toàn hơn.
- Khi tích hợp AI vào hệ thống enterprise, bảo mật và kiểm soát truy cập là yếu tố rất quan trọng.

### Ứng Dụng Vào Bản Thân

Sau sự kiện, tôi nhận thấy khi học cloud không nên chỉ tập trung vào việc deploy ứng dụng, mà cần tìm hiểu thêm về cloud operations, SRE, observability, incident response, security và cost optimization. Đây là những kiến thức giúp tôi hiểu rõ hơn cách hệ thống production được vận hành trong doanh nghiệp.

Đối với các project AI, tôi cần chú ý hơn đến domain, dữ liệu, giới hạn của model và cơ chế kiểm soát output. Nếu nghiên cứu voice agent, tôi có thể bắt đầu từ kiến trúc cơ bản STT, LLM, TTS rồi mở rộng dần sang latency, streaming và human-in-the-loop. Ngoài ra, khi xây dựng hệ thống có kết nối với dữ liệu nội bộ, tôi cần ưu tiên bảo mật, private network và kiểm soát truy cập ngay từ đầu.

### Trải Nghiệm Trong Event

Tham gia FCAJ Community Day **"Data Driven, AI Risen"** mang lại cho tôi nhiều kiến thức mới và thực tế. Sự kiện giúp tôi thấy AI không chỉ là công cụ hỗ trợ học tập hoặc viết code, mà đang được ứng dụng sâu hơn vào nhiều hoạt động doanh nghiệp như vận hành cloud, DevOps, HR analytics, voice agent và bảo mật hệ thống nội bộ.

Phần AgenticOps giúp tôi hiểu rõ hơn rằng vận hành cloud là một bài toán phức tạp và có tính critical cao. Phần voice agent giúp tôi hình dung được cách AI bằng giọng nói hoạt động và vì sao triển khai production khó hơn nhiều so với demo. Phần DevOps Agent cho thấy AI có thể hỗ trợ điều tra incident hiệu quả, còn phần HR giúp tôi thấy AI có thể mang lại giá trị cho cả những phòng ban không trực tiếp làm kỹ thuật.

Một số nội dung như MCP, ENI, Route 53 Resolver, Internal ALB, Jaeger, observability và root cause analysis vẫn còn khá mới với tôi nên cần tiếp tục tìm hiểu thêm. Tuy nhiên, chính những phần khó này giúp tôi nhận ra mình cần học sâu hơn về AWS networking, security, monitoring và production system nếu muốn theo kịp xu hướng AI trong doanh nghiệp.

### Bài Học Rút Ra

- AI đang được ứng dụng ngày càng sâu vào cloud operations, DevOps, HR, voice agent và bảo mật hệ thống.
- Cloud infrastructure càng lớn thì việc vận hành, monitoring, security và tối ưu chi phí càng quan trọng.
- AgenticOps có thể hỗ trợ xử lý incident, review code, tối ưu cost và phân tích vấn đề bảo mật.
- Voice agent production cần nhiều yếu tố hơn demo, bao gồm latency, streaming, kiểm soát output và human-in-the-loop.
- DevOps Agent giúp giảm thời gian điều tra incident nhưng vẫn cần cơ chế kiểm soát khi áp dụng vào production.
- AI trong HR giúp tăng năng suất xử lý dữ liệu nhưng không thay thế hoàn toàn vai trò con người.
- Private MCP là hướng tiếp cận quan trọng khi kết nối AI với hệ thống nội bộ trong môi trường enterprise.
- Sinh viên cần tiếp tục học thêm về cloud, security, observability và production system để chuẩn bị tốt hơn cho công việc sau này.

### Kết Luận

Thông qua FCAJ Community Day "Data Driven, AI Risen", tôi có thêm góc nhìn thực tế về cách AI đang thay đổi nhiều mảng trong doanh nghiệp, từ vận hành cloud, xử lý sự cố, xây dựng voice agent đến HR và bảo mật hệ thống nội bộ. Sự kiện giúp tôi hiểu rằng để ứng dụng AI hiệu quả, không chỉ cần biết sử dụng model mà còn phải hiểu dữ liệu, kiến trúc hệ thống, domain nghiệp vụ và cách kiểm soát rủi ro. Tôi cũng nhận ra bản thân cần chủ động học thêm về cloud operations, DevOps, security, observability và các mô hình AI agent để có nền tảng tốt hơn trong tương lai.
