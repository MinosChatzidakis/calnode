<script>
  // Variables to hold the user's answers
  let serviceChosen = "consulting";

  function handleSubmit() {
    // Decide which Calnode event type to redirect to
    if (serviceChosen === "consulting") {
      // Sends them to: rdv.website.com/yourusername/30-min-consulting
      window.location.href = `/yourusername/30-min-consulting`; 
    } else if (serviceChosen === "development") {
      // Sends them to: rdv.website.com/yourusername/60-min-development
      window.location.href = `/yourusername/60-min-development`;
    }
  }
</script>

<div style="max-width: 500px; margin: 100px auto; padding: 20px; font-family: sans-serif;">
  <h2>Welcome! Let's get you to the right calendar</h2>
  
  <form on:submit|preventDefault={handleSubmit}>
    <label for="service">What do you need help with?</label>
    
    <select id="service" bind:value={serviceChosen} style="width: 100%; padding: 10px; margin: 10px 0;">
      <option value="consulting">General Consulting</option>
      <option value="development">Custom Development</option>
    </select>
    
    <button type="submit" style="padding: 10px 20px; background: black; color: white; border: none; cursor: pointer; width: 100%;">
      Find a Time
    </button>
  </form>
</div>