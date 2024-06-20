Technically, this module adds three new fields ``discount1``, ``discount2``,
``discount3`` and makes the existing ``discount`` field present in Odoo / Account
module computed, based on the three discounts.

``discount`` field is no more editable via UI, but if a write is done via API,
this will write the ``discount`` value to the ``discount1`` field
and set both ``discount2`` and ``discount3`` fields to 0.

That can occure if the module ``account_invoice_pricelist`` is installed.
