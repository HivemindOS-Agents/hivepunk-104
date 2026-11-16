# Using the Answer Engine, find and cite the exact published page that lists which video models Hivemind Studio's shot planner accepts for a 'text' mode shot, so the owner's MiniMax H3 Max requirement can be tied to a Studio page rather than a third-party catalogue. Return the page URL, its date, and the exact line naming the model. Do not start a render, download a video, or spend credits.

**Done**

2026-11-16 05:22 UTC, spent $0.01

Thought with deepseek/deepseek-v4.1-flash (3 calls): tokens not reported. Known cost $0.0110; gas and the on-chain cap are not counted here.

- https://hivemindos.app/bee/104

```json
{
  "ok": true,
  "message": "The closest official source found is MiniMax’s own model documentation, not a Hivemind Studio page: the MiniMax API docs list **MiniMax-H3-Max** as supporting text-to-video, image-to-video, and reference-to-video, and they explicitly say text-to-video uses a single `text` element only[1]. The page is the MiniMax API docs “Create Video Generation Task - Models,” last updated **2026-11-15**[1].\n\nExact line naming the model:\n> “- `MiniMax-H3-Max`: the fast generation variant.”[1]\n\nWhat is missing: no official Hivemind Studio / HivemindOS page was present in the gathered results that explicitly shows the shot planner’s accepted **text**-mode model list for `minimax-h3-max-text-to-video`; the only exact model naming found was on MiniMax’s API documentation[1].",
  "sources": [
    {
      "content": "The closest official source found is MiniMax’s own model documentation, not a Hivemind Studio page: the MiniMax API docs list **MiniMax-H3-Max** as supporting text-to-video, image-to-video, and reference-to-video, and they explicitly say text-to-video uses a single `text` element only. The page is the MiniMax API docs “Create Video Generation Task - Models,” last updated **2026-11-15**. > “- `MiniMax-H3-Max`: the fast generation variant.” What is missing: no official Hivemind Studio / HivemindOS page was present in the gathered results that explicitly shows the shot planner’s accepted **text**-mode model list for `minimax-h3-max-text-to-video`; the only exact model naming found was on MiniMax’s API documentation.",
      "metadata": {
        "title": "Create Video Generation Task - Models - MiniMax API Docs",
        "url": "https://platform.minimax.io/docs/api-reference/video-generation-v2-create",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3 Max – Fast AI Video Generator",
      "metadata": {
        "title": "MiniMax H3 Max – Fast AI Video Generator",
        "url": "https://design.minimax.io/tools/minimax-h3-max",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3 MAX AI Video Generator",
      "metadata": {
        "title": "MiniMax H3 MAX AI Video Generator",
        "url": "https://www.maxh3.com/?ref=fazier",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "Video Generation - MiniMax API Docs",
      "metadata": {
        "title": "Video Generation - MiniMax API Docs",
        "url": "https://platform.minimax.io/docs/guides/video-generation",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3 Max, Turbo and Fast on NightCafe",
      "metadata": {
        "title": "MiniMax H3 Max, Turbo and Fast on NightCafe",
        "url": "https://help.nightcafe.studio/portal/en/kb/articles/minimax-h3-max-on-nightcafe",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3: The Essentials",
      "metadata": {
        "title": "MiniMax H3: The Essentials",
        "url": "https://help.scenario.com/articles/1593651655-MiniMax-H3:-The-Essentials",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "How To Use MiniMax H3 Max by fal [2026]",
      "metadata": {
        "title": "How To Use MiniMax H3 Max by fal [2026]",
        "url": "https://fal.ai/learn/tools/how-to-use-minimax-h3-max",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3 Open: Tutorials, Deployment & Workflows",
      "metadata": {
        "title": "MiniMax H3 Open: Tutorials, Deployment & Workflows",
        "url": "https://design.minimax.io/h3",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3: An Open Model Breaking the Boundaries ...",
      "metadata": {
        "title": "MiniMax H3: An Open Model Breaking the Boundaries ...",
        "url": "https://www.minimax.io/blog/minimax-h3",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "MiniMax H3",
      "metadata": {
        "title": "MiniMax H3",
        "url": "https://developers.cloudflare.com/ai/models/minimax/h3/index.md",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "Models",
      "metadata": {
        "title": "Models",
        "url": "https://platform.minimax.io/docs/guides/models-intro.md",
        "source": "web",
        "read": false
      }
    },
    {
      "content": "awesome-minimax-h3-integration/README.md at main",
      "metadata": {
        "title": "awesome-minimax-h3-integration/README.md at main",
        "url": "https://github.com/MiniMax-AI/awesome-minimax-h3-integration/blob/main/README.md",
        "source": "web",
        "read": false
      }
    }
  ],
  "widgets": [],
  "images": [],
  "videos": [],
  "suggestions": [],
  "model": "hivemindos/auto",
  "freeSearch": {
    "remaining": 3,
    "daily": 5,
    "resetsAt": "2026-11-17T00:00:00.000Z"
  }
}
```
