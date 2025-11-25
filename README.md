# README

This is a placeholder README file. You can update it with project
details.
✅ 1. TÓM TẮT NỘI DUNG LITEPAPER LINERA

Linera là blockchain thế hệ mới được thiết kế cho real-time markets, đặc biệt là Prediction Markets và các ứng dụng DeFi yêu cầu độ trễ cực thấp.

Vì sao DeFi cần Linera

DeFi ngày càng mở rộng, cung cấp các công cụ phức tạp như derivatives, margining và automated strategies. Prediction markets nổi lên mạnh mẽ (như Polymarket) nhưng vẫn gặp hạn chế về tốc độ và trải nghiệm. Linera giải quyết các vấn đề cốt lõi:

⭐ Các lợi ích DeFi mang lại:

Minh bạch, kiểm chứng on-chain.

Smart contracts chống thao túng.

Thanh toán tức thì bằng stablecoin.

Tính composability của toàn hệ DeFi.

Tuy nhiên, hệ DeFi hiện tại còn hạn chế về:

Độ trễ, khả năng mở rộng.

Chi phí và UX.

Lệ thuộc oracle tập trung.

An toàn cho AI agents.

🚀 Linera giải quyết điều đó bằng Microchains
Microchains = nhiều chuỗi song song

Mỗi user có một personal chain, mọi chain đều được validator xử lý nhưng block được tạo độc lập. Kết quả:

Scalability không giới hạn

Thông lượng cao

Độ trễ thấp trên toàn cầu nhờ geographic sharding

App chains cho các ứng dụng chuyên biệt

Elastic validators tự động mở rộng công suất

⚡ 1. Latency & Throughput

Vấn đề: Prediction markets, DEX, lending… cần xử lý cực nhanh khi xảy ra sự kiện đông người.

Giải pháp Linera:

Hỗ trợ vô hạn microchains song song

Hybrid DEX: matching off-chain, settlement on-chain nhưng phân tán vào nhiều chain song song

Geographic sharding giúp latency thấp theo khu vực

📡 2. Oracles

Vấn đề: Prediction markets cần oracle nhanh, chính xác, chống thao túng.

Giải pháp Linera:

Cho phép apps query trực tiếp người dùng / oracle providers

Hỗ trợ staking, ZK proofs, TEEs

Cho phép gọi dữ liệu từ Internet trực tiếp trong block

💸 3. UX & Gas

Vấn đề: Gas spike, phí cao, UX kém.

Giải pháp:

Microchains → chi phí và độ trễ dự đoán được

Giảm tắc nghẽn → cải thiện UX

🤖 4. AI Agents

Vấn đề: AI agents hiện phụ thuộc RPC tập trung, dễ bị prompt injection & front-running.

Giải pháp:

Linera hỗ trợ MCP/GraphQL local

AI agent tương tác private, không phí, không qua RPC ngoài

🛠 Technical Overview
Microchains

Personal chains, temporary chains, public chains, app chains

Validators elastic → mở rộng theo nhu cầu

Tất cả chain chạy cùng ứng dụng nhưng dữ liệu phân tán

Clients

Đồng bộ real-time trực tiếp với validators

Sparse clients → chỉ theo dõi chain cần thiết

Frontend truy cập qua GraphQL

Geographic sharding

Mỗi chain gán vào region → latency thấp

Validators liên kết bằng mạng low-latency toàn cầu

🧩 Programming Model
Cross-chain primitives

Messages

Data blobs

Event streams

Subscriptions

Dữ liệu & trạng thái được đồng bộ giữa microchains.

Transactions

Operations (từ user chain)

Incoming message bundles (từ chain khác)

Message bouncing giúp tránh thất lạc asset

Composition

Apps gọi nhau synchronous bên trong chain

Message bundles bảo đảm atomic cross-chain

Non-deterministic ops

Personal chains cho phép:

Query API ngoài

AI inference

Heavy computation

🏗 Common Design Patterns

Ứng dụng chỉ dùng user chains → scale theo số user

Client/server app dùng app chain

User chains giảm tải app chain (ví dụ: ZK proofs, airdrop)

🎯 Kết luận

Linera mang lại:

Scalability vô hạn

Real-time UX

Oracle linh hoạt

AI integration an toàn

Kiến trúc microchain cho thế hệ DeFi và prediction markets tiếp theo
