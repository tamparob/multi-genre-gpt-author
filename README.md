# multi-genre-gpt-author

This project utilizes a chain of GPT-4, Stable Diffusion, and Anthropic API calls to generate an original fantasy novel. Users can provide an initial prompt and enter how many chapters they'd like it to be, and the AI then generates an entire novel, outputting an EPUB file compatible with e-book readers.

**A 15-chapter novel can cost as little as $4 to produce, and is written in just a few minutes.**

A few output novel examples are provided in this repo. To read one, you can download its file and view it on https://www.fviewer.com/view-epub, or install it on your Kindle, etc.

## How It Works

The AI is asked to generate a list of potential plots based on a given prompt. It then selects the most engaging plot, improves upon it, and extracts a title. After that, it generates a detailed storyline with a specified number of chapters, and then tries to improve upon that storyline. Each chapter is then individually written by the AI, following the plot and taking into account the content of previous chapters. Finally, a prompt to design the cover art is generated, and the cover is created. Finally, it's all pulled together, and the novel is compiled into an EPUB file.

## Usage

You can [run the newest version of this project in Google Colab](https://colab.research.google.com/drive/1oxLraD-W0lIH9Q_pPhJ4w-hnLqU4pPvL?usp=sharing)!

In Google Colab, simply open the notebook, add your API keys, and run the cells in order. 

In the first cell of the notebook, you can customize the prompt and the number of chapters for your novel. For example:

```python
genre = "mystery"
prompt = "in a sleepy coastal town, the story unravels around the sudden disappearance of a beloved community member."
num_chapters = 20
writing_style = "Clear and easily understandable, similar to a young adult novel. Highly descriptive and sometimes long-winded."
novel, title, chapters, chapter_titles = write_fantasy_novel(prompt, num_chapters, writing_style)
```

This will generate a mystery novel based on the given prompt with 20 chapters. Note -- prompts with less than 7 chapters tend to cause issues.

## Contributions

Contributions, issues, and feature requests are welcome!

## License

This project is [MIT](https://github.com/your_username/your_repository/blob/master/LICENSE) licensed.
