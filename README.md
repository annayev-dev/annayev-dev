  - name: Replace LAST_UPDATED marker in README
    run: |
      TIMESTAMP="Last updated: $(date -u +'%Y-%m-%d %H:%M UTC')"
      perl -0777 -pe "s/<!--LAST_UPDATED-->/<!--LAST_UPDATED-->\n\n**${TIMESTAMP}**/s" README.md > README.tmp
      mv README.tmp README.md

  - name: Commit and push
    run: |
      git config user.name "github-actions[bot]"
      git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
      if git diff --quiet; then
        echo "No changes to commit"
      else
        git add README.md
        git commit -m "chore: update README last-updated timestamp"
        git push
      fi
