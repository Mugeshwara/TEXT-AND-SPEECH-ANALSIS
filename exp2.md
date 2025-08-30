{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "execution_count": 5,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "WDCK343XO_ut",
        "outputId": "c502b5d3-c1a5-4632-b8e5-fc29b0b53771"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "--- Concordance for 'freedom' ---\n",
            "Displaying 3 of 3 matches:\n",
            "                                    Freedom is the most precious gift . People \n",
            "st precious gift . People fight for freedom . True freedom comes with responsib\n",
            "t . People fight for freedom . True freedom comes with responsibility .\n",
            "\n",
            "--- Words similar to 'freedom' ---\n",
            "\n",
            "\n",
            "--- Common contexts between 'freedom' and 'gift' ---\n",
            "No common contexts were found\n"
          ]
        },
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "[nltk_data] Downloading package punkt_tab to /root/nltk_data...\n",
            "[nltk_data]   Package punkt_tab is already up-to-date!\n"
          ]
        }
      ],
      "source": [
        "import nltk\n",
        "from nltk.text import Text\n",
        "from nltk.tokenize import word_tokenize\n",
        "nltk.download('punkt_tab')\n",
        "custom_text = \"Freedom is the most precious gift. People fight for freedom. True freedom comes with responsibility.\"\n",
        "tokens = word_tokenize(custom_text)\n",
        "text_custom = Text(tokens)\n",
        "print(\"\\n--- Concordance for 'freedom' ---\")\n",
        "text_custom.concordance(\"freedom\")\n",
        "print(\"\\n--- Words similar to 'freedom' ---\")\n",
        "text_custom.similar(\"freedom\")\n",
        "print(\"\\n--- Common contexts between 'freedom' and 'gift' ---\")\n",
        "text_custom.common_contexts([\"freedom\", \"gift\"])\n"
      ]
    }
  ]
}
