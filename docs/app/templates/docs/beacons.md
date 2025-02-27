## Beacons
See {{docs-link 'animated-beacon' 'docs.api.item' 'components/animated-beacon'}}.

In this example, emails animate between Refresh (mail icon), Trash, and the Inbox. When an email gets deleted, it is a `removedSprite`. If you refresh your inbox, the new email added is an `insertedSprite`. Both the refresh button and the trash button are beacons.

### Interruption Cases
In this demonstration, the "Delete with Undo" option shows what happens when an animation is interrupted. An email that would have been a `removedSprite` becomes a `keptSprite`. 

<DocsDemo as |demo|>
  <demo.example @name="one">
    <TransitionLogTable as |logTransition|>
      <LoggedBetweenComponents @logTransition={{logTransition}} />      
    </TransitionLogTable>
  </demo.example>

  <demo.snippet @name="between-components-snippet.hbs" @label="between-components.hbs" />
  <demo.snippet @name="between-components-snippet.js" @label="between-components.js" />
  <demo.snippet @name="sprites-snippet.css" />
</DocsDemo>
