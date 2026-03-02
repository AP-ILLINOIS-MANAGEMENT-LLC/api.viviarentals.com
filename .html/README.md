<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>TurboTenant Full Dashboard</title>
<style>
    body { font-family: Arial, sans-serif; background-color: #f7f7f7; padding: 20px; margin: 0; }
    .container { max-width: 900px; margin: 0 auto; background: #fff; border-radius: 8px; padding: 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);}
    h1, h2 { color: #333; }
    h1 { font-size: 26px; margin-bottom: 10px; }
    h2 { font-size: 20px; margin-top: 1rem; cursor: pointer; }
    table { width: 100%; border-collapse: collapse; margin-top: 1rem; }
    td { vertical-align: top; padding: 4px 8px; }
    img { max-width: 100%; display: block; }
    .profile-img { width: 125px; border-radius: 8px; }
    .divider { border-bottom: 1px solid #333; margin: 1rem 0; }
    .cta-button { display: inline-block; background-color: #7075db; color: #fff; padding: 12px 24px; text-decoration: none; font-weight: bold; border-radius: 4px; margin-top: 10px; }
    .collapsible { background-color: #eee; color: #444; cursor: pointer; padding: 10px; width: 100%; border: none; text-align: left; outline: none; font-size: 16px; border-radius: 4px; margin-top: 5px;}
    .active, .collapsible:hover { background-color: #ccc; }
    .content { padding: 0 15px; display: none; overflow: hidden; background-color: #f9f9f9; border-left: 2px solid #7075db; margin-bottom: 10px; border-radius: 4px;}
    ul { padding-left: 20px; }
    .listing-container { background: #f1f1f1; padding: 15px; border-radius: 6px; margin-top: 15px; }
    .zumper-widget { margin-top: 20px; }
</style>
</head>
<body>

<div class="container">

    <h1>TurboTenant Full Dashboard</h1>

    <!-- Profile Section -->
    <div class="section">
        <h2>Landlord Profile</h2>
        <table>
            <tr>
                <td><img src="https://www.turbotenant.com/nitropack_static/DnewKXQeUpEmvDhTCIHXdznjCdZBTuQP/assets/images/optimized/rev-5b8b1ff/www.turbotenant.com/wp-content/uploads/2023/07/app-push-screening-mobile-app2x-768x1223.png" class="profile-img" alt="Handwritten Signature"></td>
                <td>
                    <h2>Sherry Woodruff</h2>
                    <p>Landlord | Property Owner / Real Estate</p>
                    <p>VIVIA Rentals</p>
                    <p>Primary Service: Platform Integration</p>
                    <p>
                        Phone: <a href="tel:2086130338">(208) 613-0338</a><br>
                        Email: <a href="mailto:sherry@viviarentals.com">sherry@viviarentals.com</a><br>
                        Website: <a href="//www.viviarentals.com">www.viviarentals.com</a><br>
                        Address: 526 S Grant St, Stockton, CA 95203, US
                    </p>
                    <a href="https://rental.turbotenant.com/auth/signup/autopilot/personalize" class="cta-button">Create My Free Account</a>
                </td>
            </tr>
        </table>
        <div class="divider"></div>
    </div>

    <!-- GTM Dashboard Section -->
    <div class="section">
        <h2>GTM Landlord Event Workflow</h2>

        <button class="collapsible">Tags</button>
        <div class="content">
            <ul>
                <li><strong>GTM-KPMRPNJ9</strong> — Event: sign_up_landlord<br>
                    Drops: user_id, property_id, plan_type, payment_amount, signup_source<br>
                    Edits: tune_event=Registration, google_ads_conversion=Landlord Signup conversion, ga_event=sign_up_landlord
                </li>
            </ul>
        </div>

        <button class="collapsible">Triggers</button>
        <div class="content">
            <ul>
                <li><strong>Trigger: turbotenant.com</strong> — Type: ALWAYS<br>
                    Filters: Event Name = sign_up_landlord, Campaign Source contains Registration, Google Click ID contains Landlord_Signup_conversion
                </li>
            </ul>
        </div>

        <button class="collapsible">Variables</button>
        <div class="content">
            <ul>
                <li><strong>TurboTenant_UserProperty</strong> — Default: rental.turbotenant.com | Key: TT_Signup_Source</li>
            </ul>
        </div>
    </div>

    <!-- Rental Listing Preview Section -->
    <div class="section">
        <h2>Rental Listing Preview</h2>
        <div class="listing-container">
            <h3>2584 Mariposa Road, Stanley, NC 28164</h3>
            <p><strong>Bedrooms:</strong> 3</p>
            <p><strong>Bathrooms:</strong> 3</p>
            <p><strong>Square Footage:</strong> 2877 sqft</p>
            <p><strong>Contact:</strong> (208) 613-0338</p>
            <p>Sign up or inquire about this property:</p>
            <a class="cta-button" href="https://turbotenant.com/r/T3duZXI6MTA4MTY1OA==?&mode=action&oobCode=code" target="_blank">Sign Up / Apply Now</a>
        </div>
    </div>

    <!-- Zumper Interactive Widget Section -->
    <div class="section">
        <h2>Stanley, NC Rental Listings</h2>
        <div class="zumper-widget">
            <!-- Embedded Zumper widget is displayed here via tool -->
        </div>
    </div>

    <!-- Footer -->
    <div class="section">
        <p style="font-size: 12px; color: #666; text-align: center;">
            This communication is intended for the designated recipient only. Any unauthorized review, use, disclosure, or distribution is prohibited. VIVIA Rentals provides property marketing and landlord onboarding services. All information is subject to change without notice.
        </p>
    </div>

</div>

<script>
    var coll = document.getElementsByClassName("collapsible");
    for (var i = 0; i < coll.length; i++) {
        coll[i].addEventListener("click", function() {
            this.classList.toggle("active");
            var content = this.nextElementSibling;
            if (content.style.display === "block") { content.style.display = "none"; }
            else { content.style.display = "block"; }
        });
    }
</script>
</body>
</html>
