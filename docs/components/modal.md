# Modal
:::raw

<DemoContainer>
  <Button :action="() => this.$refs.reportModal.show()">Show Report Modal</Button>
  <Button :action="() => this.$refs.confirmModal.show()">Show Confirm Modal</Button>
  <ModalReport
  ref="reportModal"
  itemType="project"
  :reportTypes="['cringitude', 'rudeness', 'notgamer', 'windowsuser']"
  >
  </ModalReport>
  <ModalConfirm
    ref="confirmModal"
    title="Are you sure you want to delete this version?"
    description="This will remove this version forever (like really forever)."
    :has-to-type="true"
    proceed-label="Delete"
    confirmationText="Hello"
  >
  </ModalConfirm>
</DemoContainer>
:::

```vue
  <Button :action="() => this.$refs.reportModal.modal.show()">Show Modal</Button>
  <ModalReport
  ref="reportModal"
  itemType="project"
  :reportTypes="['cringitude', 'rudeness', 'notgamer', 'windowsuser']"
  />
```