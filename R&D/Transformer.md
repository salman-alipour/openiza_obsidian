

## سطح 1 — ضروری

این‌ها را حتماً بدان:

### 1. LLM چگونه متن را می‌بیند؟

- متن را کلمه‌به‌کلمه نمی‌فهمد، بلکه به **token** تبدیل می‌شود.
- محدودیت **context window** دارد.
- ورودی طولانی‌تر همیشه بهتر نیست.

### 2. embedding چیست؟

- متن را به بردار عددی تبدیل می‌کند.
- برای similarity search و retrieval استفاده می‌شود.
- برای matching PDF/DB خیلی مهم است.

### 3. attention خیلی کلی یعنی چه؟

- مدل هنگام تولید هر بخش، به بخش‌های مهم قبلی توجه می‌کند.
- لازم نیست فرمولش را بدانی.

### 4. چرا مدل hallucinate می‌کند؟

- چون مدل generator است، نه database
- پس برای extraction و تصمیم‌گیری باید schema و validation داشته باشی

### 5. temperature و deterministic output

- برای extraction باید temperature پایین باشد
- برای chat آزاد می‌توانی بالاتر بگذاری

این سطح برای شروع **کاملاً کافی** است.

---

## سطح 2 — مفید

اگر این‌ها را بدانی، تصمیم‌های بهتری می‌گیری:

### 1. تفاوت:

- base model
- instruct model
- chat model

### 2. تفاوت:

- generative model
- embedding model
- reranker

### 3. chunking چرا مهم است؟

- چون transformer context-limited است
- chunk اشتباه = retrieval بد

### 4. long context چه محدودیت‌هایی دارد؟

- افت دقت
- افزایش هزینه
- از دست رفتن سیگنال مهم

### 5. structured extraction چرا گاهی fail می‌شود؟

- ambiguity
- weak prompt
- noisy OCR
- model limitation

### 6. quantization و inference basics

اگر local model deploy می‌کنی:

- GGUF
- Q4 / Q5 / Q8
- RAM/VRAM tradeoff

این سطح برای تو خیلی کاربردی است، مخصوصاً چون به local LLM هم علاقه داری.

---

## سطح 3 — فقط اگر بخواهی عمیق‌تر شوی

این‌ها دیگر برای ساخت محصول اولیه ضروری نیستند:

- self-attention formula
- query/key/value mathematically
- positional encoding details
- multi-head attention internals
- transformer block architecture in depth
- pretraining objective details
- fine-tuning internals
- LoRA math
- backpropagation through transformer layers

این‌ها خوب‌اند، ولی برای کاری که تو گفتی **الزامی نیستند**.







---

## و از transformer فقط این مفاهیم را بفهم:

- token
- context window
- attention در حد شهودی
- embedding
- hallucination
- inference cost
- model size vs quality
- quantization basics