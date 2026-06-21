## What is an LLM ? 
LLM stands for

> **Large Language Model**

Let's divide it.

## Large

Because it is trained on **massive amounts of text.**

Not GB.

Not TB.

Sometimes **petabytes** of text.

Millions of books.

Billions of web pages.

Code.

Research papers.

Conversations.

---

## Language

Not English.

Language means

> Human language.

Examples

* English
* Hindi
* Gujarati
* Python
* Java
* SQL
* HTML

Programming languages are also languages.

---

## Model

A model is simply

> A mathematical function that learns patterns.

Example

Suppose you show a child

```
2
4
6
8
10
```

The child says

> "Next should be 12."

Why?

Because he learned the pattern.

LLMs do exactly this.

Instead of numbers...

they learn language.

---

## Final Definition

An LLM is

> A neural network trained on a massive amount of text whose job is to predict the next token.

Notice.

Not answer questions.

Not think.

Not search.

Not understand.

Its core job is

> **Predict the next token.**

Everything else comes from doing that extremely well.

---

## Difference between AI, ML, Deep Learning and LLM
Think of Russian dolls.

```
AI
│
├── Machine Learning
│      │
│      ├── Deep Learning
│             │
│             ├── LLM
```

Every LLM is Deep Learning.

Every Deep Learning model is Machine Learning.

Every Machine Learning model is AI.

But the opposite is not true.

---

## Artificial Intelligence (AI)

AI means

> Making machines behave intelligently.

Example

Chess Engine

Google Maps

Spam Filter

Self-driving car

Alexa

These are all AI.

---

## Machine Learning

Instead of writing rules

We allow the machine to learn rules.

Traditional Programming

```
Rules + Data
      ↓
Output
```

Machine Learning

```
Data + Answers
       ↓
Machine learns Rules
```

Example

Instead of writing

```
if email contains lottery:
    spam
```

We show

```
10 million emails

Spam

Not Spam

Spam

Spam

Not Spam
```

The computer learns.

---

## Deep Learning

Machine Learning uses many algorithms.

Like

* Decision Trees
* Random Forest
* SVM
* Logistic Regression

Deep Learning uses

> Neural Networks.

Neural Networks have many layers.

Hence

Deep Learning.

---

## LLM

LLM is simply

A Deep Learning model

trained on

language.

That's it.

---

## Why GPT is called a Language Model

Because it models

language.

Not knowledge.

Not facts.

Language.

Suppose you write

```
The capital of France is
```

The model predicts

```
Paris
```

Not because it searches.

Because

after seeing billions of sentences

it knows

```
France

↓

Capital

↓

Paris
```

is an extremely probable continuation.

---

Another example

```
Roses are red

Violets are
```

It predicts

```
blue
```

Again.

Prediction.

Not memory lookup.

---

## Why isn't it just a huge if-else statement ?
Suppose English has

100,000 words.

Imagine a conversation of only

20 words.

Possible combinations

```
100000^20
```

That's roughly

```
10^100
```

That's more than atoms in many astronomical comparisons.

You cannot write

```
if user says ...

elif ...

elif ...

elif ...
```

Even Google couldn't.

---

Instead

GPT learns probabilities.

Example

Input

```
I am feeling
```

Possible next words

```
happy

sad

hungry

sleepy

excited
```

The model gives probabilities.

```
happy      0.31

sad        0.21

hungry     0.16

sleepy     0.12

excited    0.08
```

It doesn't search.

It predicts.

---

## What is Token ?
This is the most important concept.

GPT doesn't read words.

It reads

**Tokens.**

Example

```
Hello World
```

May become

```
["Hello", " World"]
```

Another

```
unbelievable
```

May become

```
un

believ

able
```

Another

```
print("Hello")
```

May become

```
print

(

"

Hello

"

)
```

Tokens are

pieces of text.

Not necessarily words.

---

Why?

Because

computers understand numbers.

Not letters.

---
## What is a Tokenizer ?
Tokenizer is

> A translator between human language and model language.

Human writes

```
Hello friend
```

Tokenizer converts

```
Hello

friend
```

into numbers

Example

```
1543

8271
```

The model only sees

```
1543

8271
```

After generating numbers

Tokenizer converts them back

```
1543 → Hello

8271 → friend
```

Without tokenizer

GPT cannot read text.

---

Flow

```
Human

↓

Tokenizer

↓

Numbers

↓

LLM

↓

Numbers

↓

Tokenizer

↓

Answer
```
## What is Context Window ?
Imagine your short-term memory.

You remember

the last few minutes.

Not your entire life.

GPT is the same.

The Context Window is

> The maximum number of tokens the model can consider at one time while generating a response.

Think of it like a whiteboard.

```
──────────────────────────

Current Conversation

──────────────────────────
```

Once the whiteboard fills,

older content has to be removed to make space.

---


It doesn't truly "forget" in the human sense.

Each response is generated from the conversation that fits inside the model's context window.

If the conversation becomes longer than that limit, the oldest tokens are no longer included in the model's input. Once those earlier messages are out of the context window, the model can't directly use them when generating new responses.

Applications can reduce this problem by summarizing earlier parts of a conversation or retrieving relevant information from long-term storage before sending the prompt to the model.

---

## 9. Why GPT-4 can remember more than GPT-3.5

Imagine two notebooks.

GPT-3.5

```
Small Notebook
```

GPT-4

```
Large Notebook
```

A larger context window means the model can process more tokens at once. That allows it to keep track of longer conversations, larger codebases, longer documents, or more detailed instructions before older information falls out of context.

This doesn't mean the model has permanent memory. It means it has a larger working memory for the current interaction.

---

## What is Temperature?

Temperature controls

**randomness.**

Not intelligence.

Not knowledge.

Think about rolling a weighted die.

---

Temperature = 0

```
Question

↓

Highest probability answer

↓

Almost identical every time
```

Example

```
2 + 2
```

Always

```
4
```

or

```
Write Python code.

↓

Very deterministic.
```

Great for

* Coding
* SQL
* Debugging
* Math
* Legal drafting

---

Temperature = 1

More variation.

Different wording.

Same meaning.

---

Temperature = 2

Very random.

Creative.

Sometimes incorrect.

Good for

Stories

Poetry

Brainstorming

Bad for

Production code.

---

## Visual intuition

```
Temperature = 0

Paris 95%

London 2%

Rome 1%

Berlin 1%

Tokyo 1%

↓

Always Paris
```

```
Temperature = 1.5

Paris 40%

London 20%

Rome 15%

Berlin 15%

Tokyo 10%

↓

Sometimes Paris

Sometimes London

Sometimes Rome
```

The probabilities are adjusted by the temperature before the next token is selected. Higher temperature flattens the distribution, giving lower-probability tokens a better chance to be chosen.

---

## What is Top-p?

Temperature changes the shape of the probability distribution.

Top-p changes **how many candidate tokens are even considered**.

Suppose the model predicts:

| Word   | Probability |
| ------ | ----------: |
| Paris  |        0.50 |
| London |        0.20 |
| Rome   |        0.15 |
| Berlin |        0.10 |
| Tokyo  |        0.05 |

### Top-p = 0.50

Only keep tokens until their cumulative probability reaches 0.50.

```
Paris
```

The model chooses only from that set.

---

### Top-p = 0.70

```
Paris

London
```

Now the choice is between those two.

---

### Top-p = 0.95

```
Paris

London

Rome

Berlin
```

A much larger pool of possible next tokens is available.

---

## Temperature vs Top-p

| Temperature                                                     | Top-p                                                                                |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Changes how "peaked" or "flat" the probability distribution is. | Chooses the smallest set of tokens whose cumulative probability reaches a threshold. |
| Higher values increase randomness.                              | Higher values allow a wider range of candidate tokens.                               |
| Controls creativity by reshaping probabilities.                 | Controls creativity by limiting the candidate pool.                                  |

In practice, many applications adjust **either** temperature **or** top-p, rather than both aggressively, because both influence randomness.

---

### Mental Model to Remember

```
Artificial Intelligence
        │
        ▼
Machine Learning
        │
        ▼
Deep Learning
        │
        ▼
Large Language Model
        │
        ▼
Tokenizer converts text → tokens
        │
        ▼
Tokens become numbers
        │
        ▼
Neural Network predicts the next token
        │
        ▼
Temperature and Top-p influence token selection
        │
        ▼
Tokenizer converts numbers → text
        │
        ▼
Response appears
```

---

## Why does an LLM predict the next token instead of the next sentence?

### Short Answer

Because predicting one token at a time is much simpler and allows the model to generate text of any length.

---

### Imagine this

Suppose I say

```
The capital of France is
```

Should the model predict the entire sentence?

```
The capital of France is Paris, which is famous for the Eiffel Tower and...
```

That would be extremely difficult.

Instead it predicts

```
Paris
```

Now the sentence becomes

```
The capital of France is Paris
```

Next prediction

```
.
```

Then

```
It
```

Then

```
is
```

Then

```
famous
```

One token at a time.

---

### Why is this better?

Because every prediction uses everything generated before it.

```
Input

↓

Predict Token 1

↓

Append Token

↓

Predict Token 2

↓

Append Token

↓

Predict Token 3

↓

...
```

This makes generation flexible.

The model can generate

* one word
* one sentence
* one paragraph
* an entire book

using the exact same process.

---


## Why can't an LLM be implemented as a giant if-else program?

### Imagine this

Suppose someone says

```
Hello
```

Easy.

```
if input == "Hello":
    print("Hi")
```

Now another person says

```
Hello bro
```

Another rule.

```
if input == "Hello bro":
```

Another person

```
Hello brother
```

Another rule.

Another

```
Hi
```

Another rule.

Another

```
Hey
```

Another rule.

Soon

```
millions

↓

billions

↓

trillions
```

of combinations appear.

---

### Human language is infinite.

People can write

```
Can you explain Python?

Could you explain Python?

Teach me Python.

Explain Python like I'm five.

Show Python basics.
```

Same meaning.

Different wording.

You cannot write rules for every possibility.

---

### What LLM does instead

Instead of rules

it learns

patterns.

Instead of

```
if sentence == ...
```

it calculates

```
Probability(next token | previous tokens)
```

Much more powerful.

---

## What is the difference between a word and a token?

People think

```
1 word = 1 token
```

This is false.

---

Example

```
Cat
```

One word.

Usually one token.

---

Example

```
Unbelievable
```

One word.

May become

```
Un

believ

able
```

Three tokens.

---

Example

```
print("Hello")
```

Could become

```
print

(

"

Hello

"

)
```

Many tokens.

---

### Why?

Because some pieces appear very frequently.

Example

```
ing

tion

pre

un

able
```

The tokenizer learns these common pieces.

---

## Why does an LLM need a tokenizer?

Computers don't understand

```
Hello
```

They understand

```
010101...

Numbers

Vectors
```

---

Tokenizer acts like a translator.

```
Human

↓

Hello friend

↓

Tokenizer

↓

1543

8271

↓

Model

↓

1543

9002

↓

Tokenizer

↓

Hello everyone
```

Without tokenizer

the model cannot understand text.

---

### Another example

Imagine givi ng Hindi to someone who only understands Japanese.

Need translator.

Tokenizer is that translator.

---

## Why does a larger context window help with long conversations?

Imagine you're writing on a whiteboard.

Small whiteboard

```
──────────────────
Today's work
──────────────────
```

After some time

No space.

You erase old information.

---

Now imagine

Huge whiteboard.

```
──────────────────────────────────────────────
Everything from the last hour
──────────────────────────────────────────────
```

Now you don't erase.

You keep everything.

---

LLMs work similarly.

The context window is their working memory for a single request.

A larger context window means the model can see more of the previous conversation, code, or document at once.

---

### Example

Suppose you're writing

5000 lines of Python.

Small context

Model forgets earlier functions.

Large context

Model still sees them.

Better answers.

---

## If you increase temperature, what changes—and what does NOT change?

Most beginners think

Temperature

↓

Model becomes smarter.

Wrong.

---

Temperature only changes

how the model chooses among possible next tokens.

Example

Prediction

| Word   | Probability |
| ------ | ----------: |
| Paris  |         90% |
| London |          5% |
| Rome   |          3% |
| Tokyo  |          2% |

---

Temperature = 0

Almost always

```
Paris
```

---

Temperature = 1.5

Maybe

```
London

Rome

Tokyo
```

more often than before.

---

### What changes?

✅ Creativity

✅ Diversity

✅ Randomness

---

### What doesn't change?

❌ Knowledge

❌ Training data

❌ Intelligence

❌ Reasoning capability

The model is exactly the same.

Only the sampling strategy changes.

---

## How is top-p different from temperature?

This is one of the most common interview questions.

---

Suppose probabilities are

| Word   | Probability |
| ------ | ----------: |
| Paris  |         50% |
| London |         20% |
| Rome   |         15% |
| Berlin |         10% |
| Tokyo  |          5% |

---

## Temperature

Changes the probabilities themselves.

Maybe after applying a higher temperature

| Word   | Probability |
| ------ | ----------: |
| Paris  |         35% |
| London |         22% |
| Rome   |         18% |
| Berlin |         15% |
| Tokyo  |         10% |

The distribution becomes flatter, making lower-probability tokens more likely to be selected.

---

## Top-p

Leaves the probabilities as they are but limits the pool of candidates.

Top-p = 0.70

Keep

```
Paris

London
```

because

```
50%

+

20%

=

70%
```

Ignore everything else.

Selection only happens from that smaller set.

---

### Simple analogy

Imagine you're choosing a restaurant.

**Temperature**

Changes how adventurous you feel.

* Low temperature → You almost always pick your favorite.
* High temperature → You're more willing to try something different.

**Top-p**

Changes the list of restaurants you're willing to consider.

* Top-p = 0.5 → Only your top favorite is on the list.
* Top-p = 0.9 → Your top five favorites are on the list.

---