You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "DAKSHINA-KANNADA MUTUAL BENEFIT NIDHI LIMITED",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/6d95c421cfdc25743ca3bee482775041.css",
    "context": {
      "path": "css/6d95c421cfdc25743ca3bee482775041.css"
    }
  },
  {
    "path": "css/827fd34f9214e869c8b614f913aef7d5.css",
    "context": {
      "path": "css/827fd34f9214e869c8b614f913aef7d5.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css",
    "context": {
      "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/127eabd8867b55dae69ba560a124fb6e.webp",
    "context": {
      "refs": [
        {
          "alt": "loansagainstdeposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/182d91658ca357fa671ef67107fb84e8.webp",
    "context": {
      "refs": [
        {
          "alt": "Recurring Deposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a97ef80f2814b48557d6f5f2297fe7a.webp",
    "context": {
      "refs": [
        {
          "alt": "HomeLoan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57ce15a006ffdb013aa3bc2dae17d20d.webp",
    "context": {
      "refs": [
        {
          "alt": "GoldLoan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c8a7d61d9d334eba957f34235ab723c.webp",
    "context": {
      "refs": [
        {
          "alt": "Housing Loan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6414e836098ebc6a45dfa96de8e1cc07.webp",
    "context": {
      "refs": [
        {
          "alt": "Daily Deposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6cd41674c98cb9c3891baf70f641c4d8.webp",
    "context": {
      "refs": [
        {
          "alt": "Loan Against Property",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/738d8e648d2279340e635740ec8dca14.webp",
    "context": {
      "refs": [
        {
          "alt": "Monthly Income Plan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76aef7d1fcd645a5bad630f821782c72.webp",
    "context": {
      "refs": [
        {
          "alt": "Loan Against Deposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a674a42054dfc6423ad3880e5a6b0019.webp",
    "context": {
      "refs": [
        {
          "alt": "RecurringDepositandFixedDeposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8e90642904015be3884074374a301c6.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4ab86cb5abeb74355032f714e194310.webp",
    "context": {
      "refs": [
        {
          "alt": "Gold Loan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c22074b18ff89edc2e61022923ca56be.webp",
    "context": {
      "refs": [
        {
          "alt": "Savings Account",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4369c477b538271e522c3c00158e92d.webp",
    "context": {
      "refs": [
        {
          "alt": "dailydepositaccounta",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6495b336c1aeb17cfa6861327424e6f.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/de5b8372a0703d641c3253fa91e149b7.webp",
    "context": {
      "refs": [
        {
          "alt": "savingsaccoun",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec1010f19829cdd90b2fdd98be070abc.webp",
    "context": {
      "refs": [
        {
          "alt": "Fixed Deposit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "DAKSHINA-KANNADA MUTUAL BENEFIT NIDHI LIMITED",
      "first_heading": "DAKSHINA-KANNADA MUTUAL BENEFIT NIDHI LIMITED"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "privacy-policy.html",
    "context": {
      "title": "DAKSHINA-KANNADA MUTUAL BENEFIT NIDHI LIMITED",
      "first_heading": ""
    }
  },
  {
    "path": "refund-policy.html",
    "context": {
      "title": "DAKSHINA-KANNADA MUTUAL BENEFIT NIDHI LIMITED",
      "first_heading": ""
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.