.. i18n: .. index::
.. i18n:    single: analytic; accounts
..

.. index::
   single: analytic; accounts

.. i18n: Putting Analytic Accounts in Place
.. i18n: ==================================
..

使辅助核算项到位
==================================

.. i18n: For the initial setup of good analytic accounts you should:
..

为能更好的初始化辅助核算您应该做到:

.. i18n: * set up the chart of accounts,
.. i18n: 
.. i18n: * create the different journals,
.. i18n: 
.. i18n: * link the analytic journals to your accounting journals.
..

* 设置会计科目表,

* 创建不同的分类帐,

* 将辅助核算关联到分类帐上.

.. i18n: Setting up the Chart of Accounts
.. i18n: --------------------------------
..

设置科目表
--------------------------------

.. i18n: Start by choosing the most suitable analytic representation for your company before entering it into OpenERP. To create the different analytic accounts, use the menu :menuselection:`Accounting--> Configuration --> Analytic Accounting --> Analytic Accounts` and click the :guilabel:`Create` button.
.. i18n: Note that the data you see when creating an analytic account will depend upon the business applications installed.
..

开始进入OpenERP之前请选择最时候贵公司的辅助核算方案。要创建不同的辅助核算项，使用菜单 :menuselection:`Accounting--> Configuration --> Analytic Accounting --> Analytic Accounts` 并点击 :guilabel:`Create` 按钮。
注意您创建辅助核算项时看到数据依赖于您已经安装的模块。

.. i18n: .. figure::  images/account_analytic_form.png
.. i18n:    :scale: 75
.. i18n:    :align: center
.. i18n: 
.. i18n:    *Setting up an Analytic Account*
..

.. figure::  images/account_analytic_form.png
   :scale: 75
   :align: center

   *配置辅助核算项*

.. i18n: To create an analytic account, you have to complete the main fields:
..

要创建一个辅助核算项，您必须完成如下字段：

.. i18n: * the :guilabel:`Account Name`,
.. i18n: 
.. i18n: * the :guilabel:`Code/Reference`: used as a shortcut for selecting the account,
.. i18n: 
.. i18n: * the :guilabel:`Parent Analytic Account`: use this field to define the hierarchy between the accounts.
.. i18n: 
.. i18n: * the :guilabel:`Account Type`: just like general accounts, the \ ``View``\ type is used for virtual accounts which are used only to create a hierarchical structure and for subtotals, and not to store accounting entries. The \ ``Normal``\ type will be used for analytic accounts containing entries.
..

*  :guilabel:`（辅助核算项）名称`,

*  :guilabel:`Code/Reference`: 用于选择辅助核算项的快捷方式,

*  :guilabel:`Parent Analytic Account`: 使用这个字段来定义不同辅助核算项的层次结构。

*  :guilabel:`Account Type`: 就像通用科目表一样,  \ ``View``\ 类型仅用于创建用于层次结构和数据汇总的虚拟项目，不能用来录入数据。  \ ``Normal``\ 类型用于包含数据的辅助核算项。

.. i18n: If an analytic account (e.g. a project) is for a limited time, you can define a start and end date here.
..

如果一个辅助核算项（特别是一个项目）有时间限制，您可以在此定义一个开始时间和结束时间。

.. i18n: The :guilabel:`Maximum Time` can be used for contracts with a fixed limit of hours to use.
..

 :guilabel:`Maximum Time` 可用于一个有固定持续时间的合同。

.. i18n: .. index::
.. i18n:    single: invoicing
..

.. index::
   single: invoicing

.. i18n: .. tip:: Invoicing
.. i18n: 
.. i18n:         You have several methods available to you in OpenERP for automated invoicing:
.. i18n: 
.. i18n:         * Service companies usually use invoicing from purchase orders, analytic accounts or
.. i18n:           project management tasks.
.. i18n: 
.. i18n:         * Manufacturing and trading companies more often use invoicing from deliveries or customer purchase
.. i18n:           orders.
.. i18n: 
.. i18n:         For more information about invoicing from projects, we refer to the book (soon to be released) about Project and Services Management.
..

.. tip:: 发票

        在OpenERP中你有几种方法可用于自动发票：

        * 服务型公司通常因采购订单，辅助核算项或项目管理任务而开具发票。

        * 制造业或贸易企业经常因发货或客户采购订单而开具发票。
          orders.

        如需要项目发票的更多信息，请参阅有关项目和服务管理的书（即将发布）。

.. i18n: Once you have defined the different analytic accounts, you can view your chart through the menu :menuselection:`Accounting --> Charts --> Chart of Analytic Accounts`. You can display analytic accounts for one or more periods or for an entire financial year.
..

一旦您定义了不同的辅助核算，您就可以通过菜单 :menuselection:`Accounting --> Charts --> Chart of Analytic Accounts` 查看清单。 您可以一个会计年度中一个或多个会计期间的辅助核算项目。

.. i18n: .. figure::  images/account_analytic_chart.png
.. i18n:    :scale: 85
.. i18n:    :align: center
.. i18n: 
.. i18n:    *Analytic Chart of Accounts*
..

.. figure::  images/account_analytic_chart.png
   :scale: 85
   :align: center

   *辅助核算表*

.. i18n: .. index::
.. i18n:    single: module; hr_timesheet_invoice
.. i18n:    single: module; account_analytic_analysis
..

.. index::
   single: module; hr_timesheet_invoice
   single: module; account_analytic_analysis

.. i18n: .. tip:: Setting up an Analytic Account
.. i18n: 
.. i18n:         The setup screen for an analytic account can vary according to the modules installed in your database.
.. i18n:         For example, you will see information about recharging services only if you have the module :mod:`hr_timesheet_invoice` installed.
.. i18n: 
.. i18n:         Some of these modules add helpful management statistics to the analytic account. The most useful is probably the module :mod:`account_analytic_analysis`, which adds such information as indicators about your margins, invoicing amounts, and latest service dates and invoice dates.
..

.. tip:: 设置辅助核算项

        辅助核算项设置画面可因安装在帐套中的模块而有很大不同。例如仅当您安装了 :mod:`hr_timesheet_invoice` 模块后才能看到有关收取服务成本费用的信息。

        这些模块增加了一些对管理有用的针对辅助核算项的统计表。最有用的可能是模块 :mod:`account_analytic_analysis` ，它增加了利润率、发票金额和最新的服务日期和发票日期等信息。

.. i18n: Creating Journals
.. i18n: -----------------
..

创建辅助核算账簿
-----------------

.. i18n: Once the analytic chart has been created for your company, you have to create the different journals.
.. i18n: These journals enable you to categorise the different accounting entries by their type, such as:
..

一旦为您的公司创建了辅助核算一览表那么您必须建立不同的帐簿。这谢帐簿可使您按不同类型的会计分录进行分录，比如：

.. i18n: * services,
.. i18n: 
.. i18n: * expense reimbursements,
.. i18n: 
.. i18n: * purchases of materials,
.. i18n: 
.. i18n: * miscellaneous expenditure,
.. i18n: 
.. i18n: * sales.
..

* 服务，

* 费用报销，

* 材料采购，

* 其他指出，

* 销售。

.. i18n: .. index::
.. i18n:    single: journal; minimal journals
..

.. index::
   single: journal; minimal journals

.. i18n: .. note::  Minimal Journals
.. i18n: 
.. i18n:         At a minimum, you have to create one analytic journal for Sales and one for Purchases.
.. i18n:         If you do not create these two, OpenERP will not validate invoices linked to an analytic account,
.. i18n:         because it would not be able to create an analytic accounting entry automatically.
..

.. note::  最小分类帐

        至少，您必须分别创建一个销售和采购辅助核算帐簿。如果您没有创建这两个帐簿，OpenERP不会验证关联到辅助核算的发票，因为它不能自动创建一个辅助核算分录。
        
.. i18n: .. figure::  images/account_analytic_journal.png
.. i18n:    :scale: 85
.. i18n:    :align: center
.. i18n: 
.. i18n:    *Creating an Analytic Journal*
..

.. figure::  images/account_analytic_journal.png
   :scale: 85
   :align: center

   *创建辅助核算账簿*

.. i18n: To define your analytic journals, use the menu :menuselection:`Accounting --> Configuration --> Analytic Accounting --> Analytic Journals` then click the :guilabel:`Create` button.
..

要定义辅助核算分类账，使用菜单 :menuselection:`Accounting --> Configuration --> Analytic Accounting --> Analytic Journals` 然后点击 :guilabel:`Create` 按钮。

.. i18n: It is easy to create an analytic journal. Just give it a :guilabel:`Journal Name`, a :guilabel:`Journal Code` and a :guilabel:`Type`. The
.. i18n: types available are:
..

很容易创建辅助核算分类账，进需给一个 :guilabel:`Journal Name`, 一个 :guilabel:`Journal Code` 和一个 :guilabel:`Type`. 可用类型有：

.. i18n: * \ ``Sale``\, for sales to customers and for credit notes,
.. i18n: 
.. i18n: * \ ``Purchase``\, for purchases and expenses,
.. i18n: 
.. i18n: * \ ``Cash``\, for financial entries,
.. i18n: 
.. i18n: * \ ``Situation``\, to adjust accounts when starting an activity, or at the end of the financial year,
.. i18n: 
.. i18n: * \ ``General``\, for all other entries.
..

* \ ``Sale``\, 适用于销售给客户和欠款，

* \ ``Purchase``\, 适用于采购和费用,

* \ ``Cash``\, 适用于凭证分录,

* \ ``Situation``\, 开始运作时的调整科目, 或在本会计年度结束时,

* \ ``General``\, 其他分录。

.. i18n: The analytic journal now has to be linked to your general journals to allow OpenERP to post the analytic entries. For example, if you enter an invoice for a customer, OpenERP will automatically search for the analytic journal of type \ ``Sales``\ linked to your Sales Journal.
.. i18n: Go to :menuselection:`Accounting--> Configuration --> Financial Accounting --> Journals --> Journals` and select for instance the Sales journal. In the :guilabel:`Analytic Journal` select the analytic sales journal.
..

辅助核算现在已链接到您的通用分类帐以便OpenERP放置辅助核算分录。比如，如果您在为客户录入发票，OpenERP 会自动搜索类型为 \ ``Sales``\ 的辅助核算关联到销售分类帐上。
通过菜单 :menuselection:`Accounting--> Configuration --> Financial Accounting --> Journals --> Journals` 并选择比方销售分类帐。 在 :guilabel:`Analytic Journal` 中也选择销售辅助分类帐。

.. i18n: .. figure::  images/account_general_journal.png
.. i18n:    :scale: 85
.. i18n:    :align: center
.. i18n: 
.. i18n:    *Linking an Analytic Journal to a Journal*
..

.. figure::  images/account_general_journal.png
   :scale: 85
   :align: center

   *关联辅助核算分类账到分类账*

.. i18n: Working with Analytic Defaults
.. i18n: ------------------------------
..

默认辅助核算项(方案)
------------------------------

.. i18n: You can work with analytic default accounts in OpenERP by installing the :mod:`account_analytic_default` module. Notice that this module is also linked with the :mod:`sale`, :mod:`stock` and :mod:`procurement` modules.
..

安装 :mod:`account_analytic_default` 模块后您可以在OpenERP中使用默认辅助核算项。 注意这个模块和 :mod:`sale`, :mod:`stock` 以及 :mod:`procurement` 模块有关联。

.. i18n: The system will automatically select analytic accounts according to the following criteria:
..

系统会根据以下条件选择辅助核算项:

.. i18n: * Product
.. i18n: * Partner
.. i18n: * User
.. i18n: * Company
.. i18n: * Date
..

* 按 所选产品 产生默认
* 按 所选业务伙伴 产生默认
* 按 登陆用户 产生默认
* 按 所选公司 产生默认
* 按 日期 产生默认

.. i18n: You can configure these criteria using the menu :menuselection:`Accounting --> Configuration --> Analytic Accounting --> Analytic Defaults` and clicking the `Create` button.
.. i18n: According to the criteria you define here, the correct analytic account will be proposed when creating an order or an invoice.
..

您可以通过菜单 :menuselection:`Accounting --> Configuration --> Analytic Accounting --> Analytic Defaults` 并点击 `Create` 按钮创建这些标准。
根据您在此定义的条件，当创建订单或发票时系统将推荐正确的辅助核算项。

.. i18n: .. figure::  images/account_analytic_default.png
.. i18n:    :scale: 85
.. i18n:    :align: center
.. i18n: 
.. i18n:    *Specify Criteria to Automatically Select Analytic Account*
..

.. figure::  images/account_analytic_default.png
   :scale: 85
   :align: center

   *提供条件以自动选择辅助核算项*

.. i18n: .. Copyright © Open Object Press. All rights reserved.
..

.. Copyright © Open Object Press. All rights reserved.

.. i18n: .. You may take electronic copy of this publication and distribute it if you don't
.. i18n: .. change the content. You can also print a copy to be read by yourself only.
..

.. You may take electronic copy of this publication and distribute it if you don't
.. change the content. You can also print a copy to be read by yourself only.

.. i18n: .. We have contracts with different publishers in different countries to sell and
.. i18n: .. distribute paper or electronic based versions of this book (translated or not)
.. i18n: .. in bookstores. This helps to distribute and promote the OpenERP product. It
.. i18n: .. also helps us to create incentives to pay contributors and authors using author
.. i18n: .. rights of these sales.
..

.. We have contracts with different publishers in different countries to sell and
.. distribute paper or electronic based versions of this book (translated or not)
.. in bookstores. This helps to distribute and promote the OpenERP product. It
.. also helps us to create incentives to pay contributors and authors using author
.. rights of these sales.

.. i18n: .. Due to this, grants to translate, modify or sell this book are strictly
.. i18n: .. forbidden, unless Tiny SPRL (representing Open Object Press) gives you a
.. i18n: .. written authorisation for this.
..

.. Due to this, grants to translate, modify or sell this book are strictly
.. forbidden, unless Tiny SPRL (representing Open Object Press) gives you a
.. written authorisation for this.

.. i18n: .. Many of the designations used by manufacturers and suppliers to distinguish their
.. i18n: .. products are claimed as trademarks. Where those designations appear in this book,
.. i18n: .. and Open Object Press was aware of a trademark claim, the designations have been
.. i18n: .. printed in initial capitals.
..

.. Many of the designations used by manufacturers and suppliers to distinguish their
.. products are claimed as trademarks. Where those designations appear in this book,
.. and Open Object Press was aware of a trademark claim, the designations have been
.. printed in initial capitals.

.. i18n: .. While every precaution has been taken in the preparation of this book, the publisher
.. i18n: .. and the authors assume no responsibility for errors or omissions, or for damages
.. i18n: .. resulting from the use of the information contained herein.
..

.. While every precaution has been taken in the preparation of this book, the publisher
.. and the authors assume no responsibility for errors or omissions, or for damages
.. resulting from the use of the information contained herein.

.. i18n: .. Published by Open Object Press, Grand Rosière, Belgium
..

.. Published by Open Object Press, Grand Rosière, Belgium
