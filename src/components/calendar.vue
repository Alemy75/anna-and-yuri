<template>
    <table class="iksweb">
        <thead>
            <tr>
                <td>Пн</td>
                <td>Вт</td>
                <td>Ср</td>
                <td>Чт</td>
                <td>Пт</td>
                <td>Сб</td>
                <td>Вс</td>
            </tr>
        </thead>
        <tbody>

            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>4</td>
                <td>5</td>
                <td>6</td>
                <td>7</td>
            </tr>
            <tr>
                <td>8</td>
                <td>9</td>
                <td>10</td>
                <td>11</td>
                <td>12</td>
                <td>13</td>
                <td>14</td>
            </tr>
            <tr>
                <td>15</td>
                <td>16</td>
                <td class="heart">❤</td>
                <td>18</td>
                <td>19</td>
                <td>20</td>
                <td>21</td>
            </tr>
            <tr>
                <td>22</td>
                <td>23</td>
                <td>24</td>
                <td>25</td>
                <td>26</td>
                <td>27</td>
                <td>28</td>
            </tr>
            <tr>
                <td>29</td>
                <td>30</td>
                <td>31</td>
                <td></td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
        </tbody>
    </table>
</template>

<style lang="scss">
@import "../style.scss";

table.iksweb {

    border-collapse: collapse;
    border-spacing: 0;
    height: auto;
}

table.iksweb,
table.iksweb td,
table.iksweb th {
    border: 2px dashed #b4b4b4;
}

table.iksweb td,
table.iksweb th {
    padding: 3px;
    width: 30px;
    height: 30px;
    text-align: center;
}

table.iksweb thead tr {
    background: color-mix(in srgb, $green 48%, transparent);
    color: #fff;
    font-weight: normal;
}

.heart {
    color: color-mix(in srgb, $green 48%, transparent);
    font-size: 20px;
}
</style>