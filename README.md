<div style="font:11px/1.35em Verdana, Arial, Helvetica, sans-serif;">
<table cellspacing="0" cellpadding="0" border="0" width="98%" style="margin-top:10px; font:11px/1.35em Verdana, Arial, Helvetica, sans-serif; margin-bottom:10px;">
<tr>
    <td align="left" valign="top">
        <!-- [ header starts here] -->
        <table cellspacing="0" cellpadding="0" border="0" width="650">
            <tr>
                <td valign="top"><a href="{{store url=""}}"><img src="{{media url="wysiwyg/logo_mail.png"}}"  alt="{{var store.getFrontendName()}}"  style="margin-bottom:10px;" border="0"/></a></td>
            </tr>
        </table>
        <!-- [ middle starts here] -->
        <table cellspacing="0" cellpadding="0" border="0" width="650">
            <tr>
                <td valign="top">
                    <p>
                        <strong>Hej {{var order.getCustomerName()}}</strong>,<br/>
                        Vi har nu færdigbehandlet din ordre og fremsender hermed din faktura.<br><br>
                        Du kan ses status p&aring; din ordre ved at <a href="{{store url="customer="customer"/account/"}}" style="color:#1E7EC8;">logge ind p&aring; din konto</a>.<br><br>
						Har du brug for kundeservice, kan du kontakte os på vores chat-support på hjemmesiden eller ringe til os på {{config path='general/store_information/phone'}}.
					</p>
      <h3 style="border-bottom:2px solid #eee; font-size:1.05em; padding-bottom:1px; ">
                        Din faktura #{{var invoice.increment_id}} for ordre #{{var order.increment_id}}
                    </h3>
                    <table cellspacing="0" cellpadding="0" border="0" width="100%">
                        <thead>
                        <tr>
                            <th align="left" width="48.5%" bgcolor="#041a3d" style="padding:5px 9px 6px 9px; border:1px solid #a9a9a9; border-bottom:none; line-height:1em;"><font color="#FFFFFF">Faktureringsinformation:</th>
                            <th width="3%"></th>
                            <th align="left" width="48.5%" bgcolor="#041a3d" style="padding:5px 9px 6px 9px; border:1px solid #a9a9a9; border-bottom:none; line-height:1em;"><font color="#FFFFFF">Betalingsmetode:</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td valign="top" style="padding:7px 9px 9px 9px; border:1px solid #a9a9a9; border-top:0; background:#FFFFFF;">
                                {{var order.billing_address.format('html')}}Email: {{var order.getCustomerEmail()}}
                            </td>
                            <td>&nbsp;</td>
                            <td valign="top" style="padding:7px 9px 9px 9px; border:1px solid #a9a9a9; border-top:0; background:#FFFFFF;">
                                {{var payment_html}}
                            </td>
                        </tr>
                        </tbody>
                    </table>
                    <br/>
                    {{depend order.getIsNotVirtual()}}
                    <table cellspacing="0" cellpadding="0" border="0" width="100%">
                        <thead>
                        <tr>
                            <th align="left" width="48.5%" bgcolor="#041a3d" style="padding:5px 9px 6px 9px; border:1px solid #a9a9a9; border-bottom:none; line-height:1em;"><font color="#FFFFFF">Leveringsinformation:</th>
                            <th width="3%"></th>
                            <th align="left" width="48.5%" bgcolor="#041a3d" style="padding:5px 9px 6px 9px; border:1px solid #a9a9a9; border-bottom:none; line-height:1em;"><font color="#FFFFFF">Leveringsmetode:</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td valign="top" style="padding:7px 9px 9px 9px; border:1px solid #a9a9a9; border-top:0; background:#FFFFFF;">
                                {{var order.shipping_address.format('html')}}
                                &nbsp;
                            </td>
                            <td>&nbsp;</td>
                            <td valign="top" style="padding:7px 9px 9px 9px; border:1px solid #ba9a9a9; border-top:0; background:#FFFFFF;">
                                {{var order.shipping_description}}&nbsp;
                            </td>
                        </tr>
                        </tbody>
                    </table>
                    <br/>
                    {{/depend}}

                    {{layout area="frontend" handle="sales_email_order_invoice_items" invoice=$invoice order=$order}}

                    <p>{{var comment}}</p>
                    <p>
      <p class="text"><span class="text"><span class="text"><b>De sikreste hilsner,</b><br />
{{config path="general/store_information/name"}}<br>
{{config path="general/store_information/address"}}<br><p>Følg os på: <a href="http://www.facebook.com/safegear" target="_blank" title="Følg os på Facebook og få gratis sikkerhedsråd"><img src="http://www.safegear.dk/media/social_icons/facebook.png">Facebook</a> <a href="http://www.linkedin.com/company/safegear-aps" target="_blank" title="Følg os på Linkedin"><img src="http://www.safegear.dk/media/social_icons/linkedin.png">LinkedIn</a>  <a href="http://www.twitter.com/safegear" target="_blank" title="Følg os på Twitter"><img src="http://www.safegear.dk/media/social_icons/twitter.png">Twitter</a></p><br>
P.S. Du kan ses status p&aring; din ordre ved at <a href="{{store url="customer="customer"/account/"}}" style="color:#1E7EC8;">logge ind p&aring; din konto</a>.
                    </p><br><hr>
<br />
</blockquote></td>
  </tr>
        </table>
    </td>
</tr>
</table>
</div>
