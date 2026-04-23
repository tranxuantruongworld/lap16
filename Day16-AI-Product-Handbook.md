## 8. Final submission — Day 16 Package

```markdown
# Day 16 Submission — Team

## Members
- Trần Xuân Trường

---

## 1. Idea reframed

Original idea:
> Hệ thống AI hỗ trợ quản lý đơn hàng cho chuỗi cửa hàng bánh mì, tự động xác nhận và điều phối đơn giữa các chi nhánh khi hết hàng.

Reframed as a product opportunity:
> Khách hàng sẽ hỗ trợ nhận đơn tự động trong giờ cao điểm, điều phối đơn hàng qua nhiều cửa hàng tối ưu chi phí và tiện lợi cho người dùng

---

## 2. Customer / Segment Card

- **Segment name:** Chuỗi bánh mì Take-away nội đô
- **Operational context:** Các chuỗi có từ 5-15 điểm bán, tập trung tại các quận trung tâm, có lượng đơn hàng online (Grab, ShopeeFood) chiếm trên 40% doanh thu.
- **Recurring workflow:** Nhận đơn -> Kiểm tra tồn kho tại chỗ -> Xác nhận đơn -> Chuẩn bị bánh -> Gọi Shipper.
- **Pain moment:** Khách đặt đơn trên App, nhân viên loay hoay kiểm tra khay bánh, thấy hết hàng nên phải hủy đơn của khách, dẫn đến mất doanh thu và bị App phạt giảm hiển thị.
- **Why now:** Sự bùng nổ của các mô hình "Cloud Kitchen" và áp lực tối ưu chi phí vận hành khi giá nguyên liệu đầu vào tăng cao.
- **Access path:** Tiếp cận qua các đơn vị cung cấp máy POS hoặc các hội nhóm chủ kinh doanh F&B chuỗi.

One-sentence description:
> Các chủ chuỗi bánh mì đang đau đầu vì tỷ lệ hủy đơn, chậm đơn cao do lệch tồn kho giữa các chi nhánh và chi phí vận chuyển đơn lẻ đắt đỏ.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- Statement (JTBD): Khi cửa hàng hiện tại hết loại bánh khách cần, tôi muốn hệ thống tự động chuyển đơn sang chi nhánh gần nhất còn hàng, để tôi không bị mất đơn hàng đó.

- Current workaround: Nhân viên gọi điện hỏi các chi nhánh khác hoặc từ chối đơn hàng của khách.

- Pain signal: Tỷ lệ hủy đơn (Cancellation rate) tại các chi nhánh vào giờ cao điểm lên tới 15-20%.

- Evidence / proxy evidence: Các chủ quán thường xuyên than phiền về việc "khách thì có mà bánh thì hết" trên các diễn đàn chủ quán F&B.

- Why underserved: Các phần mềm POS hiện tại chỉ quản lý tồn kho tĩnh, không có khả năng tự động điều hướng đơn hàng (routing) theo thời gian thực.

### Need #2
- Statement (JTBD): Khi có nhiều đơn hàng trong cùng một khu vực, tôi muốn hệ thống gom đơn để tối ưu quãng đường giao hàng, giúp tôi giảm chi phí vận chuyển trên mỗi ổ bánh.

- Current workaround: Gọi shipper đơn lẻ cho từng đơn ngay khi đơn nổ ra.

- Pain signal: Chi phí giao hàng chiếm tỷ trọng quá lớn trong giá vốn, làm biên lợi nhuận của bánh mì vốn đã thấp lại càng thấp hơn.

- Evidence / proxy evidence: Xu hướng sử dụng các dịch vụ giao hàng gom đơn (Batching) của các bên thứ 3 nhưng chưa được tích hợp sâu vào quy trình làm bánh.

- Why underserved: Logistics cho thực phẩm nóng (bánh mì) yêu cầu tốc độ cao, các thuật toán gom đơn thông thường chưa tối ưu được độ trễ giữa "lúc nướng bánh" và "lúc shipper đến".

---

## 4. Strategy Statement

For các chuỗi bánh mì nội đô
who struggle with tỷ lệ hủy đơn cao và chi phí vận chuyển đắt đỏ,
our product helps them tối ưu hóa doanh thu trên toàn chuỗi và giảm 20% chi phí ship
through cơ chế tự động điều phối đơn hàng dựa trên tồn kho thực tế,
unlike các phần mềm POS truyền thống chỉ quản lý tại chỗ,
because we can leverage khả năng phân tích dữ liệu bán hàng lịch sử để dự báo tồn kho và tối ưu hóa lộ trình giao hàng theo thời gian thực.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel (Lợi thế nhờ dữ liệu đặc thù ngành)

If we deploy 100 times in chuỗi bánh mì nội đô, the following improve:

1. Độ chính xác của dự báo tồn kho theo từng khung giờ (giảm sai lệch giữa App và thực tế).

2. Tốc độ ghép đơn (Batching efficiency) tăng lên khi mật độ đơn hàng trong hệ thống dày đặc hơn.

3. Thuật toán chọn cửa hàng dự phòng tối ưu nhất về cả "thời gian làm bánh" lẫn "quãng đường ship".

Why competitors cannot easily replicate this:

Đối thủ (POS lớn) thường làm đa ngành nên không thể tối ưu sâu cho quy trình sản xuất bánh mì (vốn có đặc thù là bánh ra lò theo mẻ và vòng đời rất ngắn). Dữ liệu điều phối vận chuyển đặc thù của chúng tôi tạo ra rào cản về hiệu quả chi phí mà một phần mềm tổng quát không thể đạt được.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | 2.500 Tỷ | Toàn bộ chi tiêu cho phần mềm quản lý (POS, CRM, Delivery) của các SMB F&B tại Đông Nam Á. | medium  |
| SAM | 500 Tỷ | 50.000 cửa hàng F&B "Digital-ready" tại Việt Nam (có bán qua app ship, ưu tiên phân khúc trung/cao cấp). | medium  |
| SOM | 6 Tỷ | 1.000 khách hàng mục tiêu đầu tiên tại các khu vực mật độ cao của Hà Nội (Cầu Giấy, Đống Đa, Hai Bà Trưng, Vinhome,...). | high |

**Top 3 unknowns requiring further research:**
1. Khả năng tích hợp (API) của các bên giao hàng (Grab, Shopee) có cho phép chuyển đổi địa điểm lấy hàng tự động hay không?

2. Mức độ sẵn sàng chia sẻ dữ liệu tồn kho real-time của nhân viên tại cửa hàng.

Chi phí t3. hực tế để duy trì hệ thống AI xử lý luồng đơn lớn so với phí subscription mà chủ quán sẵn sàng trả.

**Judgment:**
- [ ] Worth pursuing now
- [x] Worth pursuing but not now (need to validate [...] first)
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Một "trung tâm điều hành thông minh" giúp chuỗi bánh mì tự động hóa việc nhận đơn và điều phối kho bãi để không bỏ lỡ khách hàng.

**What we are not / not yet:**
> Chúng tôi không phải là một phần mềm POS thay thế hoàn toàn hệ thống tính tiền hiện có, mà là một lớp tối ưu chạy phía trên để tăng hiệu suất.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích nào team đang yếu nhất?

> Strategy (Execution side): Việc tích hợp sâu vào quy trình vận hành thực tế của cửa hàng và các nền tảng giao hàng bên thứ ba là một thử thách kỹ thuật và quan hệ đối tác lớn.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. MVP tối giản nhất để chứng minh được việc "giảm tỷ lệ hủy đơn" mà không cần tích hợp quá phức tạp là gì?

2. Làm sao để nhân viên cửa hàng tin tưởng và làm theo sự điều phối của AI thay vì làm theo thói quen?

3. Cách thiết kế luồng xác nhận đơn tự động mà vẫn đảm bảo tính cá nhân hóa cho khách hàng (ghi chú đặc biệt).
```

---

## 9. Bridge to Day 17

Day 16 đã trả lời:
- Real opportunity đằng sau idea là gì?
- Ai là early customer?
- Need thật là gì?
- Product move đúng là gì?
- Moat nào có thể compound?
- Thị trường có đáng để theo đuổi không?

Day 17 sẽ trả lời:
- **What exactly do we build first?** (MVP scope)
- Viết PRD thế nào?
- Assumption nào cần validate trước tiên?
- Experiment nào chạy trong 2 tuần đầu?

---

## 10. References

### Core readings

1. **The Lean Product Playbook** — Dan Olsen.
   [https://leanproductplaybook.com/](https://leanproductplaybook.com/)
   Gốc của Lean Product thinking (Problem Space vs Solution Space, Product-Market Fit Pyramid).

2. **TAM, SAM, and SOM: Made Simple for Growing Businesses** — Salesforce.
   [https://www.salesforce.com/blog/tam-sam-som/](https://www.salesforce.com/blog/tam-sam-som/)
   Giới thiệu cơ bản và dễ hiểu về market sizing.

### Further reading (optional, nếu team muốn đào sâu hơn)

3. **Jobs to Be Done: Theory to Practice** — Anthony W. Ulwick.
   Kinh điển về JTBD framework.

4. **The Mom Test** — Rob Fitzpatrick.
   Cách phỏng vấn khách hàng mà không bị "mom answer" làm lệch kết quả. Rất liên quan đến phần *evidence vs proxy evidence*.

5. **7 Powers: The Foundations of Business Strategy** — Hamilton Helmer.
   Phân tích 7 loại moat (Scale Economies, Network Economies, Counter-Positioning, Switching Costs, Branding, Cornered Resource, Process Power).

6. **Competing Against Luck** — Clayton Christensen.
   Case-driven, giải thích JTBD qua nhiều ví dụ đời thực.

### Quick reference — các câu chốt Day 16

| Lúc nào nhớ câu nào |
|---|
| "Respect the idea, but do not trust its first product definition." |
| "Interest is not willingness to pay." |
| "FOMO AI is not a need." |
| "A real need hurts even before AI exists." |
| "Do not sell a tool people must configure; sell a result people can use." |
| "Durable advantage comes from repeated workflow learning." |
| "Market sizing is meaningful only after product logic becomes sharper." |

---

*Chúc các bạn có một Day 16 đầy tension tốt và những câu hỏi đúng.*
