<template>
  <div class="Sidebar">
    <h1>Let us help you focus on your work!</h1>
    <p>Contact us today and we’ll make sure that happens.</p>

    <div name="formblock">
      <form method="POST" name="contact" data-netlify="true">
        <input type="hidden" name="form-name" value="contact" />
        <ul class="form-fields">
          <li class="field field-text">
            <label for="Question1" class="visuallyhidden">
              Full Name <span class="required">*</span>
            </label>

            <input
              id="Question1"
              class="Sidebar-input"
              name="Question1"
              placeholder="Full Name *"
              type="text"
              value=""
            />
          </li>
          <li class="field field-email">
            <label for="Question2" class="visuallyhidden">
              Email <span class="required">*</span>
            </label>

            <input
              id="Question2"
              class="Sidebar-input"
              name="Question2"
              placeholder="Email *"
              type="email"
              value=""
            />
          </li>
          <li class="field field-telephone">
            <label for="Question3" class="visuallyhidden"> Phone </label>

            <input
              id="Question3"
              class="Sidebar-input"
              name="Question3"
              placeholder="Phone"
              type="tel"
              value=""
            />
          </li>
          <li class="field field-textarea">
            <label for="Question4" class="visuallyhidden">
              Brief description of how we can help
              <span class="required">*</span>
            </label>

            <textarea
              id="Question4"
              name="Question4"
              class="Sidebar-input"
              placeholder="Brief description of how we can help *"
              cols="50"
              rows="3"
            ></textarea>
          </li>
        </ul>

        <div class="form-actions">
          <button type="submit" name="Submit" class="btn btn-primary submit">
            Send Away
          </button>
        </div>
      </form>
    </div>
 <img
      alt="Oracle Gold Partner"
      src="~/assets/images/SlatePreferredPartner_Silver.png"
    />
    <img
      alt="Oracle Gold Partner"
      src="~/assets/images/oracle-gold-partner.png"
    />
  </div>
</template>

<script setup></script>

<style>
@media only screen and (min-width: 1024px) {
  .Sidebar {
    padding-left: 20px;
  }
}
.Sidebar-input {
  display: block;
  width: 100%;
}
.field {
  display: block;
}
.form-actions {
  margin-top: 1em;
}
</style>
