# Lorem Insight

This is a tool for generating fake placeholder Insights for [Insights Explorer](https://github.com/ExpediaGroup/insights-explorer).  It creates Markdown files using a combination of lorem ipsum and realistic-looking text.

While created to be used in the Insights Explorer, it can be used in other contexts.  Insights Explorer uses a superset of GitHub Markdown, so some of the features of the generated files may not work in other tools.

## Example

> # Introduction
> Lorem ipsum dolor sit amet, consectetur adipisicing elit.  The following is an example of a measure that can be used to measure the effectiveness of your software. If you are using a measurement tool, you need to set up a custom ut labore et ils sont ésécriques et les régions les plus communes de l’Europe déjà dans les années 1970. Long-term interest rates have been in the range of between 2.5 and 3.0 percent.
> 
> Non est ad astra mollis e terris via. Quod tibi, quod septembre.
>
> – Lavoris, mamis. Vedi pervers We've come to the conclusion that the universe is infinite, and we're not going to find the answer to it. It's a matter of time. And we've already seen the big bang.
> 
> # Key Findings
> 
> This is the best way to book hotels online. We have thousands of hotels in all the major cities. We have hotels for every budget. No matter if you are travelling alone or with your family, we have neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed et growth-oriented community.
>
> “I’m excited to see the community come together to create a new community that is focused on the growth of the technology,” said John O‘Connor, Chief Executive Officer. Non est ad astra mollis e terris via. Quisque luctus velit. Vivamus id dolor. Etiam dolore eget tortor. Arguably the most important change we can make to the way we use technology in our lives.

## Usage

Uses Python 3.8 and [pipenv](https://pipenv.pypa.io/en/latest/):

```sh
pipenv install
pipenv run python lorem.py
```

There are two arguments to configure the ML model and the number of documents to generate.  By default it uses [EleutherAI/gpt-neo-125M](https://huggingface.co/EleutherAI/gpt-neo-125M) and generates a single document.

```sh
pipenv run python lorem.py --model EleutherAI/gpt-neo-125M --count 1
```

```sh
pipenv run python lorem.py --model google/reformer-crime-and-punishment --count 5
```

Files are generated in the `output/` directory.

## Language Models

The following models have been tested successfully:

- EleutherAI/gpt-neo-125M
- EleutherAI/gpt-neo-1.3B
- EleutherAI/gpt-neo-2.7B
- distilgpt2
- google/reformer-crime-and-punishment

## Text Generation

This script generates text using an unfiltered language model, and thus may inadvertantly generate undesirable content.  Please review the generated text before using it.

## License

[![GitHub license](https://img.shields.io/badge/license-MIT-lightgrey.svg?maxAge=2592000)](https://github.com/baumandm/lorem-insight/blob/main/LICENSE)